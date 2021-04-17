---
title: Elemento Reference (obsoleto)
description: Elemento Reference (obsoleto)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metaarchivos de Windows Media, elemento de referencia
- Metafiles, elemento Reference
- elemento Reference
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704716"
---
# <a name="reference-element-deprecated"></a>Elemento Reference (obsoleto)

En este tema se documenta una característica que ya no se usa en la versión actual de los metaarchivos de Windows Media.

El elemento **Reference** contiene una lista de referencias a direcciones URL. Cada elemento de la lista tiene el formato Ref *XX*  =  *URL*, donde *XX* es un entero y *URL* es la dirección URL de un archivo de formato de sistema avanzado (ASF).

**Sintaxis**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



Los enteros representados por *XX* deben estar en orden ascendente. Es decir, el entero de cada línea debe ser mayor que el entero de la línea anterior.

Cuando un programa cliente Lee un elemento de referencia, intenta conectarse al archivo multimedia representado por la primera dirección URL de la lista. Si se produce un error, el programa cliente intenta conectarse al archivo representado por la siguiente dirección URL de la lista. El programa cliente continúa hacia abajo en la lista hasta que realiza una conexión correcta o alcanza el final de la lista. Tenga en cuenta que si el programa cliente realiza una conexión correcta, no lee ninguna de las direcciones URL siguientes en la lista.

**Código de ejemplo**

En el ejemplo siguiente, el programa cliente primero intentaba conectarse al archivo representado por la dirección URL de MMS. Si se produjo un error, el programa cliente intentará conectarse al archivo representado por la dirección URL http.


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>Observaciones

El formato de archivo ASF abarca una amplia variedad de tipos de medios, como audio y vídeo. Los archivos ASF también usan varias extensiones de nombre de archivo diferentes, entre las que se incluyen. WMA y. wmv.

Los enteros representados por *XX* deben estar en orden ascendente. Es decir, el entero de cada línea debe ser mayor que el entero de la línea anterior.

Cuando un programa cliente Lee un elemento de referencia, intenta conectarse al archivo multimedia representado por la primera dirección URL de la lista. Si se produce un error, el programa cliente intenta conectarse al archivo representado por la siguiente dirección URL de la lista. El programa cliente continúa hacia abajo en la lista hasta que realiza una conexión correcta o alcanza el final de la lista. Tenga en cuenta que si el programa cliente realiza una conexión correcta, no lee ninguna de las direcciones URL siguientes en la lista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Versiones anteriores de los metaarchivos de Windows Media (en desuso)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




