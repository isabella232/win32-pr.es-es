---
title: Registro de coordenadas de textura (HLSL VS Reference)
description: Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértices.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149576"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registro de coordenadas de textura (HLSL VS Reference)

Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértices.

Un registro consta de propiedades que determinan el comportamiento de cada registro.



| Propiedad        | Descripción   |
|-----------------|---------------|
| Nombre            | oT0 - oT7     |
| Count           | Ocho vectores |
| Permisos de e/s | Solo escritura    |



 

Los registros de coordenadas de texturas de salida son una matriz de registros de datos de salida. Los datos de registro se iteran y se usan como coordenadas de textura en las fases de muestreo de textura para proporcionar datos al sombreador de píxeles.

Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente. Controlan los valores que se pasan con un modificador. Por ejemplo, use. XY para un mapa de textura 2D.

Las marcas de canalización de vértices de función fija, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), se deben establecer en cero si se usa un sombreador de vértices programable.

Los datos de vértices de objeto proporcionan coordenadas de textura de entrada. Los objetos que no usan texturas en mosaico suelen tener coordenadas de textura en el intervalo de \[ 0 a 1 \] . Los objetos que usan texturas en mosaico, como Terrain, normalmente tienen coordenadas de textura que van desde \[ -n, + n, \] donde n puede ser cualquier número de punto flotante.

La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización. Durante la rasterización, las coordenadas de textura se interpolan entre los vértices del objeto, se modifican mediante el ajuste de textura y se escalan según el tamaño de la textura (también teniendo en cuenta los modos de direccionamiento de textura) para generar un índice de entero. A continuación, el índice se utiliza para realizar una búsqueda de textura. Use el valor MaxTextureRepeat de [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para determinar el número de veces que se puede poner en mosaico una textura.

## <a name="example"></a>Ejemplo

Declare el registro de coordenadas de textura.


```
dcl_texcoord v7
```



Copie las coordenadas de textura por vértice en el registro de salida.


```
mov oT0, v7
```





| Versiones del sombreador de vértices      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 