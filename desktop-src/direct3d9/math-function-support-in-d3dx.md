---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152321"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="math"></a>Matemáticas

La compatibilidad con matemáticas, contenida en un conjunto de funciones, se proporciona para:

-   Cálculos de color
-   Planos
-   Manipulación de la matriz
-   Cuaterniones
-   vectores 2D
-   vectores 3D
-   4D (vectores)

Tenga en cuenta que, cuando se combina con las sobrecargas de C++, la compatibilidad con los tipos básicos de matemáticas 3D es extensa.

Para obtener más información sobre estas funciones, consulte [funciones de D3DX](dx9-graphics-reference-d3dx-functions.md). Para ayudar a encontrar la función que necesita, se dividen en varias carpetas.

## <a name="float16"></a>FLOAT16

Al usar el tipo de datos FLOAT16, asegúrese de limitar los valores a un máximo de D3DX \_ 16F \_ Max. Cualquier valor de FLOAT16 que supere esto dará lugar a un comportamiento indefinido en la canalización. Vea [otras constantes de D3DX](other-d3dx-constants.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



