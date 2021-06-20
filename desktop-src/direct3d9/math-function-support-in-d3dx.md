---
description: Obtenga información sobre la compatibilidad con funciones matemáticas en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407528"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="math"></a>Matemáticas

La compatibilidad matemática, contenida en un conjunto de funciones, se proporciona para:

-   Cálculos de color
-   Aviones
-   Manipulación de matriz
-   Cuaterniones
-   Vectores 2D
-   Vectores 3D
-   Vectores 4D

Tenga en cuenta que, cuando se combina con las sobrecargas de C++, la compatibilidad con los tipos matemáticos 3D básicos es amplia.

Para obtener más información sobre estas funciones, vea [Funciones D3DX](dx9-graphics-reference-d3dx-functions.md). Para ayudar a encontrar la función que necesita, se divide en varias carpetas.

## <a name="float16"></a>FLOAT16

Al usar el tipo de datos FLOAT16, asegúrese de limitar los valores a un máximo de D3DX \_ 16F \_ MAX. Cualquier valor FLOAT16 que supere esto dará lugar a un comportamiento indefinido en la canalización. Vea [Otras constantes D3DX](other-d3dx-constants.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



