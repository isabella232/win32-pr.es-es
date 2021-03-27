---
title: Usar la vinculación del sombreador
description: Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793587"
---
# <a name="using-shader-linking"></a>Usar la vinculación del sombreador

Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución. La vinculación del sombreador se admite a partir de Windows 8.1.

**Objetivo:** Obtenga información sobre cómo usar la vinculación de sombreador.

## <a name="prerequisites"></a>Requisitos previos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

**Tiempo total para completar:** 60 minutos.

## <a name="where-to-go-from-here"></a>Cómo continuar a partir de aquí

Vea también [API del compilador HLSL](dx-graphics-d3dcompiler-reference.md).

Te vamos a enseñar lo siguiente:

-   Compilar el código del sombreador
-   Cargar el código compilado en una biblioteca de sombreador
-   Enlazar los recursos de las ranuras de origen a las de destino
-   Crear gráficos de vinculación de funciones (FLGs) para los sombreadores
-   Vincular gráficos del sombreador con una biblioteca de sombreador para generar un BLOB de sombreador que el tiempo de ejecución de Direct3D puede usar

A continuación, se crea una biblioteca de sombreador y se enlazan los recursos de las ranuras de origen a las de destino.

[Empaquetado de una biblioteca de sombreador](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Gráficos de Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 