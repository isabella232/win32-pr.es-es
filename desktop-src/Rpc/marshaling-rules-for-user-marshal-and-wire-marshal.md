---
title: Serialización de reglas para user_marshal y wire_marshal
description: La especificación de OSF-DCE para calcular las referencias de los tipos de puntero incrustados requiere que se respeten las siguientes restricciones a la hora de implementar el tipo de \_ usuarios, escribir \_ UserMarshal y escribir \_ funciones de UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792795"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión

La especificación de OSF-DCE para calcular las referencias de los tipos de puntero incrustados requiere que se respeten las siguientes restricciones al implementar las <type> \_ funciones de usuario, <type> \_ UserMarshal y <type> \_ UserUnMarshal. (Las reglas y los ejemplos que se proporcionan aquí son para el cálculo de referencias. Sin embargo, las rutinas de ajuste de tamaño y de desserialización deben seguir las mismas restricciones:

-   Si el tipo de conexión es un tipo plano sin punteros, la rutina de cálculo de referencias para el tipo de userm correspondiente simplemente debe calcular las referencias de los datos según el diseño del tipo de conexión. Por ejemplo:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Tenga en cuenta que el tipo de conexión, **Long**, es un tipo plano. La función UserMarshal de identificador de identificador \_ \_ calcula las referencias de un **valor Long** siempre que \_ se le pasa un objeto de identificador de identificador.

-   Si el tipo de conexión es un puntero a otro tipo, la rutina de cálculo de referencias para el tipo de userm correspondiente debe calcular las referencias de los datos según el diseño del tipo al que apunta el tipo de conexión. El motor NDR se encarga del puntero. Por ejemplo:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Tenga en cuenta que el tipo de conexión, el **\_ tipo de conexión**, es un tipo de puntero. La función de UserMarshal de datos de identificador \_ \_ calcula las referencias de los datos relacionados con el identificador mediante el diseño HDATA, en lugar del \* diseño HDATA.

-   Un tipo de conexión debe ser un tipo de datos plano o un tipo de puntero. Si el tipo transmisible debe ser otro elemento (una estructura con punteros, por ejemplo), use un puntero al tipo deseado como el tipo de conexión.

El efecto de estas restricciones es que los tipos definidos con los atributos de serialización de \[ [**conexión \_**](/windows/desktop/Midl/wire-marshal) \] o de \[ [**cálculo de \_ referencias de usuarios**](/windows/desktop/Midl/user-marshal) \] se pueden insertar libremente en otros tipos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_serialización de cable**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**\_serialización de usuario**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[La función de tipo de \_ usuario](the-type-usersize-function.md)
</dt> <dt>

[La \_ función type UserMarshal](the-type-usermarshal-function.md)
</dt> <dt>

[El tipo \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[El tipo \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 