# Reflection on My Journey and Experience

## Course Learnings and Reflections

This project has been an invaluable experience that combined theoretical knowledge and practical implementation. I explored full-stack development, focusing on building robust and scalable APIs using FastAPI, SQLAlchemy, and Docker. The journey of implementing features, writing tests, and debugging not only improved my technical skills but also reinforced the importance of clean code and quality assurance.

The **User Search and Filtering** feature was a particularly challenging and rewarding experience. It required me to implement dynamic query building, role-based access control, pagination, and extensive testing to ensure reliability. Working on this project taught me how to tackle real-world development challenges effectively.

---

## Feature: User Search and Filtering

### Description

The **User Search and Filtering** feature was designed to enable administrators to search for users based on various attributes like username, email, or role and filter the results accordingly.

### User Story

*"As an administrator, I want to be able to search for users based on their username, email, role, or other relevant attributes and filter the user list accordingly."*

### Implementation Details

**Functionality Added:**
- Search users by email, username, first name, last name, or role.
- Support for filtering and pagination in the results.
- Validation for search columns to prevent SQL injection.
- Error handling for invalid input and empty results.

**Code Reference:**
- `app/routers/user_routes.py`: Contains the implementation of the `/users/search` endpoint.
- `tests/test_api/test_users_search.py`: Contains 10 test cases verifying the functionality.

**Technologies Used:**
- **FastAPI**: API framework.
- **SQLAlchemy**: ORM for secure query building.
- **Docker**: Containerization for deployment.

---

## Tests Implemented

Below are the 10 test cases created to validate the feature:

1. **test_search_users_by_email_success**  
   Ensures that users can be searched by email, and the correct results are returned.

2. **test_search_users_by_first_name_success**  
   Validates that users can be searched by their first name, and the results include the correct users.

3. **test_search_users_by_invalid_column**  
   Tests that an error is raised when an invalid column is used for searching.

4. **test_search_users_no_results_found**  
   Checks that the API responds with a `404` when no users match the search criteria.

5. **test_search_users_without_authorization**  
   Confirms that unauthorized users cannot access the search API.

6. **test_search_users_with_expired_token**  
   Ensures that the API rejects requests made with expired tokens.

7. **test_search_users_case_insensitive**  
   Validates that searches are case-insensitive and return appropriate results.

8. **test_search_users_pagination**  
   Confirms that the API correctly supports pagination for large result sets.

9. **test_search_users_invalid_value**  
   Checks how the API handles invalid input values for the search query.

10. **test_search_users_multiple_results**  
    Ensures that the API returns multiple results for a valid search query.

---

## Deployment to DockerHub

The application was successfully containerized and deployed to DockerHub.  
You can pull the image using the following commands:


docker pull amanjaswal/final
docker pull amanjaswal/final:41873a986f5b16e98abad1b8b4d5538abbd14542

DockerHub Repository: https://hub.docker.com/r/amanjaswal/final

## Links to Artifacts

## Closed QA Issues:
 
1. QA issue 1: [Link](https://github.com/growthinvestor/user_management/tree/1-dockerrunissue)
2. QA Issue 2: [Link](https://github.com/growthinvestor/user_management/tree/3-secondusercreationissue)
3. QA Issue 3: [Link](https://github.com/growthinvestor/user_management/tree/5-admin-role-removal-for-token)
4.	QA Issue 4: [Link](https://github.com/growthinvestor/user_management/tree/7-github-actions-workflow-issue)
5. QA Issue 5: [Link](https://github.com/growthinvestor/user_management/tree/9-fix-database-reset-issue-in-pytest)

1. New Test Cases for Feature: [Link](https://github.com/growthinvestor/user_management/blob/main/tests/test_api/test_users_search.py)

1. Feature Implementation: [Link](https://github.com/growthinvestor/user_management/tree/NewSearchFeature)

## Final Thoughts

This project has been a transformative learning experience, providing hands-on exposure to real-world development scenarios. The emphasis on clean code, testing, and deployment has given me the confidence to tackle similar challenges in the future.

Thank you for providing this opportunity to learn, build, and grow.
