# spring-data-redis-example
@EnableCaching - instructs the registered cache manager to store the result of the method call in a cache.
CommonConfig

Using the @Cacheable annotation without parameters will force Spring to use default names for both the cache and cache key.

We can override both of these behaviors by adding some parameters to the annotation:

@Service
public class AddressService {
    @Cacheable(value = "address_cache", key = "customerId")
    public AddressDTO getAddress(long customerId) {
        // lookup and return result
    }
}

The example above tells Spring to use a cache named address_cache and the customerId argument for the cache key.

@CacheEvict - to delete info from DB & reflect in cache
@CachePut - to update info in DB & reflect in cache
@Cacheable - for get API


Caffeine cache is a high-performance Cache Manager
