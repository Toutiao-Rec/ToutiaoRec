# ToutiaoRec

---

### Dataset Organization

ToutiaoRec is constructed by sampling 70 million user requests from the Toutiao feed scenario over 3 days, resulting in 313 million requests. The dataset includes real user feedback such as clicks, likes, comments, and more. For each request, we retain all exposed items, along with the ranking information across all pipeline stages.

To handle the large volume of unexposed data, we sample negatives as follows:

- **Global Random Negatives (GN)**: Randomly sampled from the entire candidate pool at a 1:2 ratio to exposed positives.
- **Ranking Negatives (RN)**: 10 unexposed candidates ranked below position 50 in the ranking stage.
- **Pre-ranking Negatives (PRN)**: 10 unexposed candidates ranked below position 200 in the pre-ranking stage.

All types of negatives retain their ranking positions from the respective stages.

In addition:

- The dataset includes 29 types of anonymized features, such as user behaviors and item attributes.
- Given the diverse content formats in Toutiao (articles, microblogs, short videos, etc.), each candidate is annotated with its content type.

The code and data will be released.
