# Redis Caching Strategy

## Cache Keys
- weather:{lat}:{lon}:7day - TTL: 6 hours
- crop_prediction:{farm_id} - TTL: 24 hours
- market_prices:{crop}:{state} - TTL: 12 hours

## Cache Invalidation
- Invalidate on new market data upload
- Invalidate farm cache on profile update
- Use cache-aside pattern for reads

## Performance Gains
- Weather API calls reduced by 85%
- Prediction latency: 450ms → 45ms
- Database load reduced by 60%
