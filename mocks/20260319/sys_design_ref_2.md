Great—here’s a **complete 45-minute mock interview script + grading rubric** you can use to practice or run interviews effectively.

---

# 🎥 45-Min Mock Interview Script: Design a YouTube-like System

(Modeled around a system like YouTube)

---

## ⏱️ 0–5 min: Problem Framing

**Interviewer prompt**

> Design a video streaming platform like YouTube.

**Strong candidate should:**

* Clarify scope:

  * “Do we need uploads + streaming?” ✅
  * “Do we include live streaming?” (optional)
  * “Scale expectations?” (millions vs billions)

**Expected clarification outcome**

* Focus: upload + VOD streaming
* Global scale
* Basic social features

---

## ⏱️ 5–10 min: Requirements

### ✅ Functional

* Upload videos
* Watch videos
* Search
* Like/comment/subscribe

### ✅ Non-functional

* Low latency playback
* High availability
* Scalability
* Durability

**Strong signal**

* Mentions *read-heavy system*
* Mentions *large file handling*

---

## ⏱️ 10–15 min: High-Level Design

Candidate should draw:

```
Client → API Gateway → App Servers
                      ↓
                Metadata DB
                      ↓
               Object Storage
                      ↓
                     CDN
```

### Key components:

* API servers (stateless)
* Metadata DB
* Blob storage
* CDN
* Processing pipeline

**Follow-up questions**

* “Where does transcoding happen?”
* “How do users stream videos efficiently?”

---

## ⏱️ 15–25 min: Deep Dive — Video Upload & Processing

### Expected Answer

**Upload**

* Chunked uploads
* Resume support

**Processing pipeline**

* Async via queue
* Steps:

  * Transcoding (multi-resolution)
  * Thumbnail generation

**Strong signals**

* Mentions **decoupling via queue (Kafka/SQS)**
* Mentions **event-driven architecture**

**Follow-up**

> What happens if processing fails?

Expected:

* Retry jobs
* Dead-letter queue

---

## ⏱️ 25–30 min: Storage & Data Design

### Expected

**Video storage**

* Object storage (S3-like)

**Metadata**

* SQL (strong consistency)

**High-write systems**

* NoSQL for comments/likes

### Bonus

* Mentions **eventual consistency for views/likes**

---

## ⏱️ 30–35 min: Content Delivery & Performance

### Expected

**CDN usage**

* Cache video chunks globally

**Streaming format**

* HLS/DASH segmentation

**Caching**

* Redis for metadata

**Strong signals**

* Mentions **hot video optimization**
* Mentions **edge caching**

---

## ⏱️ 35–40 min: Scalability & Reliability

### Expected

* Load balancers
* Horizontal scaling
* DB replication
* Multi-region setup

### Failure handling

* Upload retries
* CDN fallback to origin

---

## ⏱️ 40–45 min: Wrap-up + Advanced Topics

### Optional deep dives

Ask one:

* “How would you design recommendations?”
* “How to support live streaming?”
* “How to detect abuse?”

**Strong candidates**

* Discuss tradeoffs clearly
* Don’t over-engineer prematurely

---

# 🧪 Grading Rubric (Score out of 10)

## 1. Requirements Clarity (0–1.5)

* 0: Jumps into solution
* 1: Some clarification
* 1.5: Clearly scopes system

---

## 2. High-Level Design (0–2)

* 0: Missing major components
* 1: Basic structure
* 2: Clean, scalable architecture

---

## 3. Video Pipeline Understanding (0–2)

* 0: No pipeline
* 1: Mentions transcoding
* 2: Full async pipeline + queue + retries

---

## 4. Scalability & Performance (0–2)

* 0: No scaling strategy
* 1: Basic scaling
* 2: CDN + caching + hot video strategy

---

## 5. Storage & Data Modeling (0–1.5)

* 0: Weak DB choices
* 1: Reasonable design
* 1.5: Clear separation (blob vs metadata)

---

## 6. Tradeoffs & Depth (0–1)

* 0: No tradeoffs
* 1: Explains decisions clearly

---

## 🔑 Score Interpretation

* **9–10** → Strong hire (senior level)
* **7–8** → Solid (mid-level)
* **5–6** → Needs improvement
* **<5** → Not ready

---

# 🎯 Interviewer Cheat Sheet (Quick Prompts)

Use these if the candidate gets stuck:

* “How do we handle large file uploads?”
* “How do we stream efficiently worldwide?”
* “What happens when a video goes viral?”
* “How do you reduce latency?”

---

If you want, I can simulate a **live mock interview (I ask, you answer, I grade in real time)** or give you a **top 1% candidate answer script** that sounds exactly like a senior engineer in an interview.
