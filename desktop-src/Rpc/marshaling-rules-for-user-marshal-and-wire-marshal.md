---
title: Reglas de serialización para user_marshal y wire_marshal
description: La especificación OSF-DCE para serializar tipos de puntero incrustados requiere que se observen las restricciones siguientes al implementar el tipo UserSize, el tipo UserMarshal y las funciones \_ \_ \_ UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244472"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Reglas de serialización para la serialización \_ de usuario y la serialización de \_ conexión

La especificación OSF-DCE para serializar tipos de puntero incrustados requiere que se observen las restricciones siguientes al implementar el tipo UserSize, el tipo UserMarshal y las funciones &lt; &gt; \_ &lt; &gt; \_ &lt; &gt; \_ UserUnMarshal. (Las reglas y los ejemplos que se proporcionan aquí son para la serialización. Sin embargo, las rutinas de cambio de tamaño y desmarque deben seguir las mismas restricciones:

-   Si wire-type es un tipo plano sin punteros, la rutina de serialización para el tipo userm correspondiente simplemente debe serializar los datos según el diseño del tipo de conexión. Por ejemplo:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Tenga en cuenta que el tipo de conexión, **long**, es un tipo plano. La función HANDLE \_ HANDLE \_  UserMarshal serializa un largo cada vez que se le pasa un objeto HANDLE \_ HANDLE.

-   Si wire-type es un puntero a otro tipo, la rutina de serialización para el userm-type correspondiente debe serializar los datos según el diseño del tipo al que apunta el tipo de conexión. El motor PLACE se encarga del puntero. Por ejemplo:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Tenga en cuenta que el tipo de conexión WIRE **\_ TYPE** es un tipo de puntero. La función HANDLE DATA UserMarshal serializa los datos relacionados con el identificador mediante el diseño HDATA, en lugar \_ \_ del diseño \* HDATA.

-   Un tipo de conexión debe ser un tipo de datos plano o un tipo de puntero. Si el tipo transmisible debe ser otra cosa (una estructura con punteros, por ejemplo), use un puntero al tipo deseado como tipo de conexión.

El efecto de estas restricciones es que los tipos definidos con los atributos de serialización de conexión o de cálculo de referencias de usuario se pueden incrustar libremente \[ [**\_**](/windows/desktop/Midl/wire-marshal) en \] otros \[ [**\_**](/windows/desktop/Midl/user-marshal) \] tipos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**wire \_ marshal**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**serialización \_ de usuario**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[El tipo \_ UserSize (Función)](the-type-usersize-function.md)
</dt> <dt>

[El tipo \_ UserMarshal (Función)](the-type-usermarshal-function.md)
</dt> <dt>

[El tipo \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[Thetype \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 
