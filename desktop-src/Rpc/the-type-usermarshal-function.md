---
title: La función type_UserMarshal
description: La \_ función type UserMarshal es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421374"
---
# <a name="the-type_usermarshal-function"></a>La \_ función type UserMarshal

La función **<type> \_ UserMarshal** es una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuario](/windows/desktop/Midl/user-marshal) \] . El código auxiliar llama a esta función para calcular las referencias de los datos en el lado cliente o servidor. La función se define como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<type>En el nombre de la función se entiende el tipo de userm especificado en la definición de la **\[ \_ serialización \] de conexión** o el tipo de cálculo de **\[ \_ referencias \] del usuario** . Este tipo puede ser no transmitible o incluso cuando se usa con el atributo de **\[ \_ cálculo de referencias \] del usuario** , un tipo desconocido para el compilador de MIDL. El nombre del tipo de conexión (el nombre del tipo transmisible) no se utiliza en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de conexión de los datos tal y como se especifica en OSF DCE.

El parámetro *pFlags* es un puntero a un campo de marca larga sin signo. La palabra superior de la marca contiene marcas de representación de datos NDR tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres. La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM. El diseño exacto de las marcas dentro del campo se describe en [la función de tipo de \_ usuario](the-type-usersize-function.md).

El parámetro *pBuffer* es el puntero de búfer actual. Este puntero puede o no estar alineado en la entrada. La función **<type> \_ UserMarshal** debe alinear el puntero de búfer correctamente, calcular las referencias de los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto serializado. Tenga en cuenta que la especificación de tipo de conexión determina el diseño real de los datos en el búfer.

El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario.

El valor devuelto es la nueva posición del búfer, que es la dirección del primer byte después del objeto cuyas referencias no se han calculado.

El desbordamiento del búfer puede producirse cuando se calcula incorrectamente el tamaño de los datos e intenta calcular las referencias de más datos de los esperados. Debe tener cuidado para evitar esta situación. Puede comprobarlo con el puntero que devuelve **<type> \_ UserMarshal** . De lo contrario, corre el riesgo de que el motor NDR genere una excepción de desbordamiento de búfer más adelante.

Las excepciones deben detectarse y administrarse localmente, las excepciones no se deben permitir que propigated la pila de llamadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_serialización de cable](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_serialización de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 