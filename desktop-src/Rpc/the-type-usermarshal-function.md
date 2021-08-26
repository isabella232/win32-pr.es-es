---
title: La type_UserMarshal función
description: La función UserMarshal de tipo es una función auxiliar para los atributos \_ \wire \_ marshal\ y \user \_ marshal\.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffea134b78ae8187fce3fab7876150c0a7a8cd7f892ebac602966712ec1b60e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016475"
---
# <a name="the-type_usermarshal-function"></a>El tipo \_ UserMarshal (Función)

La **<type> \_ función UserMarshal** es una función auxiliar para los atributos \[ [wire marshal \_ y](/windows/desktop/Midl/wire-marshal) \] user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Los códigos auxiliares llaman a esta función para serializar los datos en el lado cliente o servidor. La función se define como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

en el nombre de la función significa el tipo userm especificado en la definición <type> **\[ \_ \] de** **\[ \_ \]** tipo de serialización de conexión o de cálculo de referencias de usuario. Este tipo puede no ser transmitible o incluso, cuando se usa con el atributo **\[ de \_ \]** serialización de usuario, un tipo desconocido para el compilador MIDL. El nombre del tipo de conexión (el nombre del tipo transmisible) no se usa en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de la conexión para los datos según lo especificado por OSF DCE.

El *parámetro pFlags* es un puntero a un campo de marca larga sin signo. La palabra superior de la marca contiene marcas de representación de datos de BYTE tal y como se define en OSF DCE para las representaciones de punto flotante, orden de bytes y caracteres. La palabra inferior contiene una marca de contexto de cálculo de referencias tal como se define en el canal COM. El diseño exacto de las marcas dentro del campo se describe en [El tipo \_ Función UserSize](the-type-usersize-function.md).

El *parámetro pBuffer* es el puntero de búfer actual. Este puntero puede o no estar alineado en la entrada. La **<type> \_ función UserMarshal** debe alinear el puntero de búfer correctamente, serializar los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto serializado. Tenga en cuenta que la especificación del tipo de conexión determina el diseño real de los datos en el búfer.

El *parámetro pMyObj* es un puntero a un objeto de tipo de usuario.

El valor devuelto es la nueva posición del búfer, que es la dirección del primer byte después del objeto no semarshaled.

El desbordamiento del búfer puede producirse cuando calcula incorrectamente el tamaño de los datos e intenta serializar más datos de los esperados. Debe tener cuidado de evitar esta situación. Puede comprobarlo mediante el puntero que **<type> \_ devuelve UserMarshal.** De lo contrario, corre el riesgo de que el motor HAYA producido una excepción de desbordamiento de búfer más adelante.

Las excepciones deben capturarse y controlarse localmente, no se debe permitir que las excepciones propulsen la pila de llamadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reglas de serialización para la serialización \_ de usuario y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 