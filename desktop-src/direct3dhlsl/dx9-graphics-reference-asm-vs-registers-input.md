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
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994372"
---
# <a name="input-register"></a>Registro de entrada

Registro de entrada del sombreador de vértices.

Los datos de cada vértice (mediante uno o varios flujos de vértices de entrada) se cargan en los registros de entrada de vértices antes de que se ejecute el sombreador de vértices. Los registros de entrada constan de vectores de punto flotante de componente 16 4, designados como V0 a través de V15. Estos registros son de solo lectura. Un registro de entrada se enlaza a los datos de vértice a través de una declaración de vértice.

Las siguientes propiedades de registro controlan el comportamiento de cada registro:



| Propiedad        | Descripción                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Nombre            | v \[ n \] -n es un número de registro opcional. 0 es el valor predeterminado que se usa, si se omite.     |
| Count           | Un máximo de 16 registros, V0-V15.                                                          |
| Permisos de e/s | Solo lectura. Este registro no se puede escribir en la API o en el sombreador.                   |
| Leer puertos      | 1. este es el número de veces que se puede leer un registro dentro de una única instrucción. Vea a continuación. |



 

Cualquier instrucción única solo puede tener acceso a un registro de entrada de vértice. Sin embargo, cada origen de la instrucción puede swizzle de forma independiente y negar ese vector a medida que se lee.

## <a name="example"></a>Ejemplo

Este es un ejemplo de uso de una declaración de vértice para enlazar datos de posición de vértice 2D para registrar v0.

La declaración de vértices pertenece a la aplicación:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Esta es la declaración del sombreador de vértices correspondiente:


```
dcl_position v0
```





| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posición      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




