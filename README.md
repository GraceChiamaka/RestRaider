# RestRaider
A rest api client


### Core Features to Implement:

**1. Endpoint Definition System**
- Define endpoints with path params that TypeScript extracts: `/users/:id/:postId`
- Use template literal types to parse the URL string
- Generic endpoint definition that captures request/response types

**2. Request Method Routing**
- Conditional types to determine if a body is required (GET/DELETE vs POST/PUT)
- Different method signatures based on HTTP verb
- Type-safe path parameter injection

**3. Query Builder**
- Fluent API: `api.users().where({ status: 'active' }).limit(10)`
- Each method returns a new typed builder
- Generic constraints to prevent invalid combinations

**4. Response Transformers**
- Map/transform response data with type inference
- Chain transformations while maintaining types
- Optional vs required fields based on transformation

**5. Type-Safe Error Handling**
- Discriminated unions for success/error states
- Generic Result<T, E> type
- Error types that vary by endpoint

### Challenge Milestones:

1. ✅ Basic GET with no params
2. ✅ Path parameters with type extraction
3. ✅ Query parameters (optional vs required)
4. ✅ Request body validation
5. ✅ Response type inference
6. ✅ Chained query builder
7. ✅ Multiple response format support (JSON/text/blob)
8. ✅ Middleware/interceptors with typed context
