### SD540-REST
Given the following Mongoose Schema:
```typescript
const CourseSchema = new Schema({
    code: { type: String, required: true },
    name: { type: String, required: true },
    description: String,
    deleted: { type: Boolean, default: false }
}, { timestamps: true });

const StudentSchema = new Schema({
    email: { type: String, required: true },
    name: { type: String, required: true },
    courses: [CourseSchema],
    deleted: { type: Boolean, default: false }
}, { timestamps: true });
```
Create a Rest API which allows users to perform CRUD operations on `students` and `courses` entities.
