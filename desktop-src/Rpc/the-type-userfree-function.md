---
title: La función type_UserFree
description: La \_ función type UserFree es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791733"
---
# <a name="the-type_userfree-function"></a>La \_ función type UserFree

La función **<type> \_ UserFree** es una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuario](/windows/desktop/Midl/user-marshal) \] . El código auxiliar llama a esta función para liberar los datos en el lado del servidor. La función se define como:

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<type>En el nombre de la función se entiende el tipo de userm especificado en la definición de la **\[ \_ serialización \] de conexión** o el tipo de cálculo de **\[ \_ referencias \] del usuario** .

El parámetro *pFlags* es un puntero a un campo de marca **larga sin signo** . La palabra superior de la marca contiene marcas de representación de datos NDR tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres. La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM. El diseño exacto de las marcas dentro del campo se describe en [la función de tipo de \_ usuario](the-type-usersize-function.md).

El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario. El motor NDR libera el objeto de nivel superior. Usted es responsable de liberar los objetos a los que puede apuntar el objeto de nivel superior.

Las excepciones deben detectarse y administrarse localmente, las excepciones no se deben permitir que propigated la pila de llamadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_serialización de cable](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_serialización de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 