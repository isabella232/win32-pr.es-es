---
description: El uso es similar al ámbito de un parámetro, porque define el ámbito en el que el parámetro es válido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Usos y literales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1d7b40e66aaa6499dd2aa00c37d4564df2ab
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998542"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="facc9-103">Usos y literales (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="facc9-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="facc9-104">El uso es similar al ámbito de un parámetro, porque define el ámbito en el que el parámetro es válido.</span><span class="sxs-lookup"><span data-stu-id="facc9-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



| <span data-ttu-id="facc9-105">Value</span><span class="sxs-lookup"><span data-stu-id="facc9-105">Value</span></span>  | <span data-ttu-id="facc9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="facc9-106">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="facc9-107">const</span><span class="sxs-lookup"><span data-stu-id="facc9-107">const</span></span>  | <span data-ttu-id="facc9-108">El parámetro será constante dentro del ámbito de todas las funciones.</span><span class="sxs-lookup"><span data-stu-id="facc9-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="facc9-109">(Tenga en cuenta que estos parámetros todavía se pueden escribir en [**con ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), porque esto se produce fuera del ámbito de todas las funciones).</span><span class="sxs-lookup"><span data-stu-id="facc9-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="facc9-110">shared</span><span class="sxs-lookup"><span data-stu-id="facc9-110">shared</span></span> | <span data-ttu-id="facc9-111">El parámetro se compartirá en el grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="facc9-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="facc9-112">static</span><span class="sxs-lookup"><span data-stu-id="facc9-112">static</span></span> | <span data-ttu-id="facc9-113">El parámetro será invisible para la aplicación, es decir, no se puede acceder a ellos desde [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler.**](id3dxeffectcompiler.md)</span><span class="sxs-lookup"><span data-stu-id="facc9-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="facc9-114">Marcar un parámetro como literal indica que su valor nunca cambiará.</span><span class="sxs-lookup"><span data-stu-id="facc9-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="facc9-115">Esto permite que el compilador de efectos realice una optimización adicional.</span><span class="sxs-lookup"><span data-stu-id="facc9-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="facc9-116">Solo los parámetros de nivel superior no compartidos se pueden marcar como literales.</span><span class="sxs-lookup"><span data-stu-id="facc9-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="facc9-117">Los parámetros solo se pueden marcar como literales [**con ID3DXEffectCompiler.**](id3dxeffectcompiler.md)</span><span class="sxs-lookup"><span data-stu-id="facc9-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="facc9-118">Los valores literales no se pueden establecer [**con ID3DXEffect.**](id3dxeffect.md)</span><span class="sxs-lookup"><span data-stu-id="facc9-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="facc9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="facc9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="facc9-120">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="facc9-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



