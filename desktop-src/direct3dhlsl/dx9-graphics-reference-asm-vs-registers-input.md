---
title: Registro de entrada
description: Registro de entrada
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6682d8987f2df3ba3fb06427d41b722abb5eb003a4226a155c104cc3239d0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982765"
---
# <a name="input-register"></a>Registro de entrada

Registro de entrada del sombreador de vértices.

Los datos de cada vértice (mediante uno o varios flujos de vértices de entrada) se cargan en los registros de entrada de vértice antes de ejecutar el sombreador de vértices. Los registros de entrada constan de 16 vectores de punto flotante de cuatro componentes, designados como v0 a v15. Estos registros son de solo lectura. Un registro de entrada se enlaza a los datos de vértice a través de una declaración de vértice.

Las propiedades de registro siguientes controlan cómo se comporta cada registro:



| Propiedad        | Descripción                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Nombre            | v \[ n - n es un número de registro \] opcional. 0 es el valor predeterminado utilizado, si se omite.     |
| Count           | Un máximo de 16 registros, v0 - v15.                                                          |
| Permisos de E/S | Solo lectura. La API o el sombreador no pueden escribir este registro.                   |
| Lectura de puertos      | 1. Este es el número de veces que se puede leer un registro dentro de una sola instrucción. Vea a continuación. |



 

Cualquier instrucción única solo puede tener acceso a un registro de entrada de vértice. Sin embargo, cada origen de la instrucción puede deslizar y negar ese vector de forma independiente a medida que se lee.

## <a name="example"></a>Ejemplo

Este es un ejemplo de uso de una declaración de vértice para enlazar datos de posición de vértice 2D para registrar v0.

La declaración de vértice pertenece a la aplicación:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Esta es la declaración correspondiente del sombreador de vértices:


```
dcl_position v0
```





| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de posición      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




