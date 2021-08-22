---
title: Registro de coordenadas de textura (referencia de HLSL VS)
description: Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e695765d57c7e74c94fe0605ca7ec7b96705d7b37d1dc24cad068a5aed6a2ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457765"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registro de coordenadas de textura (referencia de HLSL VS)

Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértice.

Un registro consta de propiedades que determinan cómo se comporta cada registro.



| Propiedad        | Descripción   |
|-----------------|---------------|
| Nombre            | oT0 - oT7     |
| Count           | Ocho vectores |
| Permisos de E/S | Solo escritura    |



 

Los registros de coordenadas de textura de salida son una matriz de registros de datos de salida. Los datos de registro se iteran y se usan como coordenadas de textura en las fases de muestreo de textura para proporcionar datos al sombreador de píxeles.

Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente. Controlar los valores que se pasan con un modificador . Por ejemplo, use .xy para un mapa de textura 2D.

Las marcas de canalización de vértices de función fija, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF COUNT4) deben establecerse en cero si se usa un sombreador de vértices \_ programable.

Los datos de vértice de objeto suministran coordenadas de textura de entrada. Los objetos que no usan texturas en mosaico normalmente tienen coordenadas de textura en el \[ intervalo de 0,1 \] . Los objetos que usan texturas en mosaico, como el terreno, suelen tener coordenadas de textura que van desde -n,+n, donde n puede ser \[ cualquier número de punto \] flotante.

La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización. Durante la rasterización, las coordenadas de textura se interpolan entre los vértices de objeto, se modifican mediante el ajuste de textura y se escalan por el tamaño de textura (también teniendo en cuenta los modos de direccionamiento de textura) para generar un índice entero. A continuación, el índice se usa para realizar una búsqueda de textura. Use el valor MaxTextureRepeat de [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para determinar cuántas veces se puede mosaicor una textura.

## <a name="example"></a>Ejemplo

Declare el registro de coordenadas de textura.


```
dcl_texcoord v7
```



Copie las coordenadas de textura por vértice en el registro de salida.


```
mov oT0, v7
```





| Versiones del sombreador de vértices      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 