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
# <a name="using-shader-linking"></a><span data-ttu-id="84bdc-103">Usar la vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="84bdc-103">Using shader linking</span></span>

<span data-ttu-id="84bdc-104">Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="84bdc-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="84bdc-105">La vinculación del sombreador se admite a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="84bdc-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="84bdc-106">**Objetivo:** Obtenga información sobre cómo usar la vinculación de sombreador.</span><span class="sxs-lookup"><span data-stu-id="84bdc-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="84bdc-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="84bdc-107">Prerequisites</span></span>

<span data-ttu-id="84bdc-108">Suponemos que estás familiarizado con C++.</span><span class="sxs-lookup"><span data-stu-id="84bdc-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="84bdc-109">También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="84bdc-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="84bdc-110">**Tiempo total para completar:** 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="84bdc-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="84bdc-111">Cómo continuar a partir de aquí</span><span class="sxs-lookup"><span data-stu-id="84bdc-111">Where to go from here</span></span>

<span data-ttu-id="84bdc-112">Vea también [API del compilador HLSL](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="84bdc-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="84bdc-113">Te vamos a enseñar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="84bdc-113">We show you how to:</span></span>

-   <span data-ttu-id="84bdc-114">Compilar el código del sombreador</span><span class="sxs-lookup"><span data-stu-id="84bdc-114">Compile your shader code</span></span>
-   <span data-ttu-id="84bdc-115">Cargar el código compilado en una biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="84bdc-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="84bdc-116">Enlazar los recursos de las ranuras de origen a las de destino</span><span class="sxs-lookup"><span data-stu-id="84bdc-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="84bdc-117">Crear gráficos de vinculación de funciones (FLGs) para los sombreadores</span><span class="sxs-lookup"><span data-stu-id="84bdc-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="84bdc-118">Vincular gráficos del sombreador con una biblioteca de sombreador para generar un BLOB de sombreador que el tiempo de ejecución de Direct3D puede usar</span><span class="sxs-lookup"><span data-stu-id="84bdc-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="84bdc-119">A continuación, se crea una biblioteca de sombreador y se enlazan los recursos de las ranuras de origen a las de destino.</span><span class="sxs-lookup"><span data-stu-id="84bdc-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="84bdc-120">Empaquetado de una biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="84bdc-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="84bdc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84bdc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84bdc-122">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="84bdc-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="84bdc-123">Gráficos de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="84bdc-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="84bdc-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="84bdc-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 