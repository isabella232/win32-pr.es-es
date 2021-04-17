---
description: Marca de capacidad del controlador.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705288"
---
# <a name="d3denum"></a><span data-ttu-id="51bdc-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="51bdc-103">D3DENUM</span></span>

<span data-ttu-id="51bdc-104">Marca de capacidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="51bdc-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51bdc-105">#define</span><span class="sxs-lookup"><span data-stu-id="51bdc-105">#define</span></span></td>
<td><span data-ttu-id="51bdc-106">Value</span><span class="sxs-lookup"><span data-stu-id="51bdc-106">Value</span></span></td>
<td><span data-ttu-id="51bdc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="51bdc-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51bdc-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="51bdc-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="51bdc-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="51bdc-109">0x00000002L</span></span></td>
<td><span data-ttu-id="51bdc-110">Pruebas de controladores de los laboratorios de calidad de hardware de Microsoft Windows (WHQL).</span><span class="sxs-lookup"><span data-stu-id="51bdc-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="51bdc-111">Se trata de una prueba lenta que requiere una penalización de tiempo de un segundo o dos segundos.</span><span class="sxs-lookup"><span data-stu-id="51bdc-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="51bdc-112">El miembro WHQLLevel de <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>usa esta constante.</span><span class="sxs-lookup"><span data-stu-id="51bdc-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51bdc-113">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="51bdc-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="51bdc-114">D3DENUM_WHQL_LEVEL está en desuso para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual).</span><span class="sxs-lookup"><span data-stu-id="51bdc-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="51bdc-115">Cualquiera de estos sistemas operativos devuelve 1 para el nivel de WHQL sin comprobar el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="51bdc-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="51bdc-116">Información constante</span><span class="sxs-lookup"><span data-stu-id="51bdc-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="51bdc-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51bdc-117">Header</span></span>                   | <span data-ttu-id="51bdc-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="51bdc-118">d3d9.h</span></span>     |
| <span data-ttu-id="51bdc-119">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="51bdc-119">Minimum operating system</span></span> | <span data-ttu-id="51bdc-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="51bdc-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="51bdc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51bdc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51bdc-122">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="51bdc-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




