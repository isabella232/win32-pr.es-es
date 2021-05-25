---
description: Marca de funcionalidad del controlador.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343268"
---
# <a name="d3denum"></a><span data-ttu-id="e33da-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="e33da-103">D3DENUM</span></span>

<span data-ttu-id="e33da-104">Marca de funcionalidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="e33da-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e33da-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="e33da-105">#define</span></span></td>
<td><span data-ttu-id="e33da-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e33da-106">Value</span></span></td>
<td><span data-ttu-id="e33da-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e33da-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33da-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="e33da-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="e33da-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e33da-109">0x00000002L</span></span></td>
<td><span data-ttu-id="e33da-110">Pruebas Laboratorios de calidad de hardware de Windows (WHQL) controladores de Microsoft Laboratorios de calidad de hardware de Windows (WHQL) (WHQL).</span><span class="sxs-lookup"><span data-stu-id="e33da-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="e33da-111">Se trata de una prueba que consume mucho tiempo y que requiere una penalización de tiempo de un segundo o dos segundos.</span><span class="sxs-lookup"><span data-stu-id="e33da-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="e33da-112">El miembro WHQLLevel de usa esta <a href="d3dadapter-identifier9.md"><strong>constante D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e33da-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e33da-113">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="e33da-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="e33da-114">D3DENUM_WHQL_LEVEL está en desuso para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual).</span><span class="sxs-lookup"><span data-stu-id="e33da-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="e33da-115">Cualquiera de estos sistemas operativos devuelve 1 para el nivel WHQL sin comprobar el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="e33da-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="e33da-116">Información constante</span><span class="sxs-lookup"><span data-stu-id="e33da-116">Constant Information</span></span>



| <span data-ttu-id="e33da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e33da-117">Requirement</span></span>                         | <span data-ttu-id="e33da-118">Value</span><span class="sxs-lookup"><span data-stu-id="e33da-118">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e33da-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e33da-119">Header</span></span>                   | <span data-ttu-id="e33da-120">d3d9.h</span><span class="sxs-lookup"><span data-stu-id="e33da-120">d3d9.h</span></span>     |
| <span data-ttu-id="e33da-121">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="e33da-121">Minimum operating system</span></span> | <span data-ttu-id="e33da-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e33da-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e33da-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e33da-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33da-124">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="e33da-124">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




