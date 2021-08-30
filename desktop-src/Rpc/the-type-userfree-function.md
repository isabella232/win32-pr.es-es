---
title: La type_UserFree función
description: La función \_ UserFree de tipo es una función auxiliar para los atributos \wire \_ marshal\ y \user \_ marshal\.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e852f18380ef3df01b3428badc7c7c75b70e0b03
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885667"
---
# <a name="the-type_userfree-function"></a>El tipo \_ UserFree (Función)

La **&lt; función &gt; \_ UserFree de** tipo es una función auxiliar para los atributos wire marshal \[ [ \_ y](/windows/desktop/Midl/wire-marshal) \] user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Los códigos auxiliares llaman a esta función para liberar los datos en el lado servidor. La función se define como:

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

El tipo en el nombre de función significa el tipo userm especificado en la definición &lt; &gt; **\[ de \_ \]** **\[ \_ \]** tipo de serialización de conexión o de cálculo de referencias de usuario.

El *parámetro pFlags* es un puntero a **un campo de marca larga** sin signo. La palabra superior de la marca contiene marcas de representación de datos de BYTE tal y como se define en OSF DCE para las representaciones de punto flotante, orden de bytes y caracteres. La palabra inferior contiene una marca de contexto de serialización tal como se define en el canal COM. El diseño exacto de las marcas dentro del campo se describe en [El tipo \_ Función UserSize](the-type-usersize-function.md).

El *parámetro pMyObj* es un puntero a un objeto de tipo de usuario. El motor FORMAT libera el objeto de nivel superior. Usted es responsable de liberar los objetos a los que pueda apuntar el objeto de nivel superior.

Las excepciones deben capturarse y controlarse localmente, no se debe permitir que las excepciones propulsen la pila de llamadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reglas de serialización para la serialización \_ de usuario y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
