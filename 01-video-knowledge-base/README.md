# DNS Resolution Issue — Video Script

---

## 🎥 Video Title
"How to Fix DNS Resolution Issues (Step-by-Step)"

---

## 📋 Scenario
Customer reports: "Websites are not opening. It says 'Server not found'."

---

## 🗣️ Narration Script (English)

**[0:00-0:15] Introduction**
"Hi everyone! Today we'll fix a common issue — DNS resolution failure. When this happens, websites don't open even though your internet is working."

**[0:15-0:20] What is DNS Host?**
"First, let me explain what a DNS Host is. A DNS Host is like a phonebook — it converts domain names like google.com into IP addresses that computers understand."

**[0:20-0:45] Show the Problem**
"Now let me show you what the customer is seeing."
- Open Command Prompt
- Type: `ping google.com`
- *It fails ❌*
"See? It says 'Ping request could not find host.' This means the DNS Host is not working."

**[0:45-1:15] Check Internet**
"Now let me check if the internet is actually working."
- Type: `ping 8.8.8.8`
- *It works ✅*
"Ping 8.8.8.8 is working! So internet is fine, but the DNS Host is the problem."

**[1:15-1:30] Check Current DNS Host**
"Let me check which DNS Host we are currently using."
- Type: `ipconfig /all`
- Show: `DNS Servers . . . . . . . . . . . : 192.168.1.1`
"See? We are using 192.168.1.1 as our DNS Host."

**[1:30-1:45] Test DNS Host**
"Now let me test if this DNS Host can resolve google.com."
- Type: `nslookup google.com`
- *Shows error or no response ❌*
"The DNS Host is not responding. This is why websites are not opening."

**[1:45-2:15] Fix 1: Flush DNS**
"First, let me clear the DNS cache."
- Type: `ipconfig /flushdns`
- *Shows "Successfully flushed"*
"Now let me test again."
- Type: `nslookup google.com`
- *Still fails ❌*
"Hmm, still not working. The DNS Host is still not responding."

**[2:15-3:00] Fix 2: Change DNS Host (Main Fix)**
"Now I'll change the DNS Host to Google's public DNS server — 8.8.8.8."
- Show Network Settings → IPv4 Properties
- Change to: `8.8.8.8` and `8.8.4.4`
- Click OK
"Now let me check the new DNS Host."
- Type: `ipconfig /all`
- Show: `DNS Servers . . . . . . . . . . . : 8.8.8.8`
"See? Now we are using Google's DNS Host."

**[3:00-3:30] Verify Fix**
"Now let me test if the new DNS Host can resolve google.com."
- Type: `nslookup google.com`
- *Shows IP address: 142.250.185.78 ✅*
"See? The DNS Host is now resolving google.com to IP address 142.250.185.78."

**[3:30-4:00] Final Verification**
- Type: `ping google.com`
- *It works ✅*
"Ping is working now! The issue is resolved. The new DNS Host is working correctly."

**[4:00-4:15] Closing**
"And that's how you fix DNS resolution issues by changing the DNS Host! Thanks for watching."

---

## 📊 Video Summary Card
> **Issue:** DNS Resolution Failure  
> **Fix:** Flush DNS + Change DNS Host to 8.8.8.8  
> **Time:** 4 minutes  
> **Commands:** ipconfig, ping, nslookup, ipconfig /flushdns

---

## 🛠️ Commands Used

| Command | Purpose |
|---------|---------|
| `ping google.com` | Test DNS resolution (fails) |
| `ping 8.8.8.8` | Test internet connectivity (works) |
| `ipconfig /all` | Check current DNS Host IP |
| `ipconfig /flushdns` | Clear DNS cache |
| `nslookup google.com` | Test DNS Host resolution |

---

## 🖥️ Screen Actions (Step-by-Step)

| Step | Action | What to Show |
|------|--------|--------------|
| 1 | Open Command Prompt | Windows + R → `cmd` → Enter |
| 2 | Show Problem | `ping google.com` → Fails ❌ |
| 3 | Check Internet | `ping 8.8.8.8` → Works ✅ |
| 4 | Check DNS Host | `ipconfig /all` → Show DNS IP |
| 5 | Test DNS Host | `nslookup google.com` → Fails ❌ |
| 6 | Flush DNS | `ipconfig /flushdns` → Success |
| 7 | Test Again | `nslookup google.com` → Fails ❌ |
| 8 | Change DNS Host | Network Settings → 8.8.8.8 |
| 9 | Verify DNS Host | `ipconfig /all` → Show 8.8.8.8 ✅ |
| 10 | Test Resolution | `nslookup google.com` → IP shows ✅ |
| 11 | Final Verify | `ping google.com` → Works ✅ |

---

## 📹 Video Recording (OBS)

| Step | Action |
|------|--------|
| 1 | Open OBS Studio |
| 2 | Add Display Capture source |
| 3 | Check mic is working |
| 4 | Click **Start Recording** |
| 5 | Follow the script above |
| 6 | Click **Stop Recording** |
| 7 | File → Show Recordings |
| 8 | Save video as `DNS-Resolution-Fix.mp4` |

---

## 🔗 Related Lab
`DNS_Troubleshooting_Resolution`

---

## ✅ Video Checklist (OBS)
- [ ] OBS Display Capture added
- [ ] Mic working (green bars moving)
- [ ] Explain what DNS Host is
- [ ] Show `ping google.com` → Fails ❌
- [ ] Show `ping 8.8.8.8` → Works ✅
- [ ] Show `ipconfig /all` → Current DNS Host IP
- [ ] Show `nslookup google.com` → Fails ❌
- [ ] Run `ipconfig /flushdns` → Success
- [ ] Show `nslookup google.com` → Still Fails ❌
- [ ] Change DNS to 8.8.8.8 in Network Settings
- [ ] Show `ipconfig /all` → New DNS Host 8.8.8.8 ✅
- [ ] Show `nslookup google.com` → IP Address shows ✅
- [ ] Show `ping google.com` → Works ✅
- [ ] Stop Recording
- [ ] Save video
- [ ] Upload to GitHub

---

