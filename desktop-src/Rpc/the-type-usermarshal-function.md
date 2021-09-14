---
title: La type_UserMarshal función
description: La función UserMarshal de tipo es una función auxiliar para los atributos \_ \wire \_ marshal\ y \_ \user marshal\.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42bd7ce6d9d107fe24affc895ba802e73ee8fe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171293"
---
# <a name="the-type_usermarshal-function"></a>El tipo \_ UserMarshal (Función)

La **&lt; función &gt; \_ UserMarshal de** tipo es una función auxiliar para los atributos wire marshal \[ [ \_ y](/windows/desktop/Midl/wire-marshal) \] user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Los códigos auxiliares llaman a esta función para serializar los datos en el lado cliente o servidor. La función se define como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

El tipo en el nombre de función significa el tipo userm especificado en la definición de tipo de &lt; &gt; **\[ \_ \]** **\[ \_ serialización \]** de conexión o de serialización de usuario. Este tipo puede no ser transmitible o incluso, cuando se usa con el atributo **\[ \_ de \]** serialización de usuario, un tipo desconocido para el compilador MIDL. El nombre del tipo de conexión (el nombre del tipo transmisible) no se usa en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de cable define el diseño de conexión para los datos según lo especificado por OSF DCE.

El *parámetro pFlags* es un puntero a un campo de marca larga sin signo. La palabra superior de la marca contiene marcas de representación de datos de BYTE definidas por OSF DCE para representaciones de punto flotante, orden de bytes y caracteres. La palabra inferior contiene una marca de contexto de serialización definida por el canal COM. El diseño exacto de las marcas dentro del campo se describe [en El tipo Función \_ UserSize](the-type-usersize-function.md).

El *parámetro pBuffer* es el puntero de búfer actual. Este puntero puede o no estar alineado en la entrada. La **&lt; función &gt; \_ UserMarshal** de tipo debe alinear correctamente el puntero de búfer, serializar los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto serializado. Tenga en cuenta que la especificación del tipo de conexión determina el diseño real de los datos en el búfer.

El *parámetro pMyObj* es un puntero a un objeto de tipo de usuario.

El valor devuelto es la nueva posición del búfer, que es la dirección del primer byte después del objeto no marshaled.

El desbordamiento del búfer puede producirse si calcula incorrectamente el tamaño de los datos e intenta serializar más datos de los esperados. Debe tener cuidado de evitar esta situación. Puede comprobarlo mediante el puntero que **&lt; devuelve &gt; \_ UserMarshal.** De lo contrario, se corre el riesgo de que el motor de REACTOR cree una excepción de desbordamiento de búfer más adelante.

Las excepciones se deben capturar y controlar localmente, no se debe permitir que las excepciones propigan la pila de llamadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reglas de serialización para la serialización \_ de usuarios y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
