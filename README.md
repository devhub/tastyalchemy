# tastyalchemy

SQLAlchemy object resource for django-tastypie

## Usage

    from baph.auth.models import User
    from tastyalchemy import SQLAlchemyResource

    class UserResource(SQLAlchemyResource):

        class Meta:
            resource_name = 'user'
            object_class = User
            allowed_methods = ['get', 'post', 'put', 'delete']
            excludes = ['password']
