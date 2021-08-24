---
title: Uso de la vinculación de sombreador
description: Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f382596f3839460943fdbefe5687c4e7b18401db016ad3f834284e994217b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742285"
---
# <a name="using-shader-linking"></a>Uso de la vinculación de sombreador

Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución. La vinculación del sombreador se admite a partir de Windows 8.1.

**Objetivo:** Aprenda a usar la vinculación de sombreador.

## <a name="prerequisites"></a>Requisitos previos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

**Tiempo total para completar:** 60 minutos.

## <a name="where-to-go-from-here"></a>Cómo continuar a partir de aquí

Consulte también [LAS API del compilador HLSL.](dx-graphics-d3dcompiler-reference.md)

Te vamos a enseñar lo siguiente:

-   Compilación del código del sombreador
-   Carga del código compilado en una biblioteca de sombreadores
-   Enlazar los recursos de las ranuras de origen a las ranuras de destino
-   Construcción de gráficos de vinculación de funciones (FLG) para sombreadores
-   Vincular gráficos de sombreador con una biblioteca de sombreadores para generar un blob de sombreador que el tiempo de ejecución de Direct3D puede usar

A continuación, crearemos una biblioteca de sombreador y enlazaremos recursos de ranuras de origen a ranuras de destino.

[Empaquetado de una biblioteca de sombreador](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Gráficos de Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 