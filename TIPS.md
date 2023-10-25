### TIPS
$Manejo de PropTypes

Debemos importar PropTypes
```
import PropTypes from 'prop-types';
```

A continuación describo un ejemplo con valores por defecto.

```
import PropTypes from 'prop-types';

const HelloWorld = ({user, id, title}) => {

    return (
        <>
            <h1>{title}</h1>
            <div>Que tal {user.name} {user.lastName} con el id = {id}</div>
            <div>{JSON.stringify(user)}</div>
        </>
    );
}

HelloWorld.propTypes = {
    title: PropTypes.string.isRequired,
    id: PropTypes.number.isRequired,
    user : PropTypes.object.isRequired
};

HelloWorld.defaultProps = {
    title: 'Hola mundo por defecto!'
};

export default HelloWorld;
```
