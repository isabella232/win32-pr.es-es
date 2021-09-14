---
title: La type_UserUnmarshal de trabajo
description: La función UserUnmarshal de tipo es una función auxiliar para los atributos \_ \wire \_ marshal\ y \_ \user marshal\.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05281e7ae9d25ee25b4e3198dd834c78d81c3f53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244412"
---
# <a name="the-type_userunmarshal-function"></a>El tipo \_ UserUnmarshal (Función)

La **&lt; función &gt; \_ UserUnmarshal de** tipo es una función auxiliar para los atributos wire marshal \[ [ \_ y](/windows/desktop/Midl/wire-marshal) \] user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Los códigos auxiliares llaman a esta función para desmarshal los datos en el lado cliente o servidor. La función se define como:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

El tipo en el nombre de función significa el tipo userm especificado en la definición de tipo de &lt; &gt; **\[ \_ \]** **\[ \_ serialización \]** de conexión o de serialización de usuario. Este tipo puede ser intransmitible o par ,cuando se usa con el atributo **\[ \_ de \]** serialización de usuario, desconocido para el compilador MIDL. El nombre del tipo de conexión (el nombre del tipo transmisible) no se usa en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de cable define el diseño de conexión para los datos según lo especificado por OSF DCE.

El *parámetro pFlags* es un puntero a **un campo de marca larga** sin signo. La palabra superior de la marca contiene marcas de representación de datos de BYTE definidas por OSF DCE para representaciones de punto flotante, orden de bytes y caracteres. La palabra inferior contiene una marca de contexto de serialización definida por el canal COM. El diseño exacto de las marcas dentro del campo se describe [en El tipo Función \_ UserSize](the-type-usersize-function.md).

El *parámetro pBuffer* es el puntero de búfer actual. Este puntero puede o no estar alineado en la entrada. La función **&lt; &gt; \_ UserUnmarshal** de tipo debe alinear correctamente el puntero de búfer, desmarshal los datos y devolver la nueva posición del búfer, que es la dirección del primer byte después del objeto no semarshaled.

El *parámetro pMyObj* es un puntero a un objeto de tipo definido por el usuario.

En un entorno heterogéneo, el motor ESIS realiza cualquier conversión de datos necesaria antes de llamar a la **&lt; &gt; \_ función UserUnmarshal de** tipo. Tenga en cuenta que el motor NDR lleva a cabo esta conversión de datos según la definición de tipo de conexión proporcionada para este tipo de datos de usuario. La marca indica la representación de datos del remitente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reglas de serialización para la serialización \_ de usuarios y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
