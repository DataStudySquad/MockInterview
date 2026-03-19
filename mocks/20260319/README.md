### 20210910

#### Y
- sys design:

- Here’s a cleaner, more structured version you can use to set up a strong system design mock interview prompt:

---

### 📌 Mock Interview Prompt: Design a YouTube-like Video Platform

**Problem Statement**
Design a large-scale video sharing platform similar to YouTube where users can upload, process, and stream videos to millions of viewers worldwide.

---

### 🎯 Core Requirements

**Functional Requirements**

* Users can upload videos
* Users can view/stream videos
* Support search for videos (by title, tags, etc.)
* Display video metadata (title, description, views, likes)
* Allow users to like, comment, and subscribe to channels

**Non-Functional Requirements**

* High availability and reliability
* Low latency video playback
* Scalability to handle millions of concurrent users
* Efficient storage for large video files
* Global content delivery

---

### 🧩 Discussion Areas

Encourage the candidate to walk through:

1. **High-Level Architecture**

   * Key components (API servers, storage, CDN, etc.)
   * Request flow (upload → processing → playback)

2. **Video Upload & Processing Pipeline**

   * Chunked uploads
   * Transcoding into multiple resolutions
   * Thumbnail generation

3. **Storage Design**

   * Metadata storage (SQL vs NoSQL)
   * Blob storage for videos

4. **Content Delivery**

   * Use of CDNs for global distribution
   * Caching strategies

5. **Scalability & Performance**

   * Load balancing
   * Horizontal scaling
   * Handling hot videos

6. **Database Design**

   * Schema for users, videos, comments
   * Indexing for search

7. **Reliability & Fault Tolerance**

   * Replication
   * Failover strategies

8. **Optional Deep Dives**

   * Recommendation system
   * Live streaming support
   * Abuse detection / moderation

#### A
- coding:
  - LC weekly xxx
  - Needcode all
    - https://neetcode.io/practice/practice/allNC
