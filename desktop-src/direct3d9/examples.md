---
description: A continuación se siguen dos definiciones de plantilla binarias de ejemplo y un ejemplo de un objeto de datos binarios.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Ejemplos (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888572"
---
# <a name="examples-direct3d-9-graphics"></a>Ejemplos (gráficos de Direct3D 9)

A continuación se siguen dos definiciones de plantilla binarias de ejemplo y un ejemplo de un objeto de datos binarios.

> [!Note]  
> Los datos se almacenan en formato little-endian, que no se muestra en estos ejemplos.

 

La plantilla cerrada RGB se identifica mediante el UUID {55b6d780-37ec-11d0-ab39-0020af71e433} y tiene tres miembros (r, g y b) cada uno de tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



La plantilla cerrada Matrix4x4 se identifica mediante el UUID {55b6d781-37ec-11d0-ab39-0020af71e433} y tiene un miembro (una matriz bidimensional denominada matrix) de tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



El objeto de datos binario siguiente muestra una instancia de la plantilla RGB definida anteriormente. El objeto de ejemplo se denomina azul y sus tres miembros (r, g y b) tienen los valores 0.0, 0.0 y 1.0, respectivamente.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 



