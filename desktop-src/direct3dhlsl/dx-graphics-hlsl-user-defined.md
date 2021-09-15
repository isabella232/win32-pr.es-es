---
title: Tipo definido por el usuario
description: Use la sintaxis siguiente para declarar un tipo definido por el usuario.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573772"
---
# <a name="user-defined-type"></a>Tipo definido por el usuario

Use la sintaxis siguiente para declarar un tipo definido por el usuario.



|                                           |
|-------------------------------------------|
| typedef **\[ const \] Type Name \[ Index \]**; |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[Const\]**<br/>                 | Opcional. Esta palabra clave marca explícitamente el tipo como una constante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/>     | Identifica el tipo de datos; debe ser uno de los tipos de datos intrínsecos HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Índice**<br/> | Tamaño de matriz opcional. Debe ser un entero sin signo entre 1 y 4 inclusive.<br/> |



 

Además de los tipos de datos intrínsecos integrados, HLSL admite tipos personalizados o definidos por el usuario que siguen esta sintaxis:

## <a name="remarks"></a>Observaciones

Los tipos definidos por el usuario no distinguen mayúsculas de minúsculas. Para mayor comodidad, los siguientes tipos se definen automáticamente en el ámbito super global.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



El signo de pera ( \# ) representa un dígito entero entre 1 y 4.

Para la compatibilidad con los efectos de DirectX 8, los siguientes tipos se definen automáticamente en el ámbito super global:


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





