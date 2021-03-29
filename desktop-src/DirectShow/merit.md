---
description: Los valores de mérito definen el orden en el que el administrador de gráficos de filtro intenta agregar filtros durante la creación del gráfico.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérito (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678876"
---
# <a name="merit"></a><span data-ttu-id="a5b04-103">Fundament</span><span class="sxs-lookup"><span data-stu-id="a5b04-103">Merit</span></span>

<span data-ttu-id="a5b04-104">Los valores de mérito definen el orden en el que el administrador de gráficos de filtro intenta agregar filtros durante la creación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a5b04-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="a5b04-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérito \_ Mérito preferido** (0x800000) mérito <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ normal** (0x600000) mérito <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improbable** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **mérito \_ \_ no \_ use** (0x200000) el <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ \_ compresor** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** de la mérito del software (0x100050).</span><span class="sxs-lookup"><span data-stu-id="a5b04-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="a5b04-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5b04-106">Remarks</span></span>

<span data-ttu-id="a5b04-107">Cada filtro se registra con un valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="a5b04-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="a5b04-108">Cuando el administrador de gráficos de filtro genera un gráfico, enumera todos los filtros registrados con el tipo de medio correcto.</span><span class="sxs-lookup"><span data-stu-id="a5b04-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="a5b04-109">A continuación, los prueba en orden de mérito, de mayor a menor.</span><span class="sxs-lookup"><span data-stu-id="a5b04-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="a5b04-110">(Utiliza criterios adicionales para elegir entre los filtros con el mismo mérito). Nunca intenta los filtros con un valor de mérito menor o igual que el **mérito \_ no se \_ \_ usa**.</span><span class="sxs-lookup"><span data-stu-id="a5b04-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="a5b04-111">Un filtro que nunca debe tenerse en cuenta para la reproducción normal debe tener un mérito de **mérito \_ \_ no \_ usar** o menos.</span><span class="sxs-lookup"><span data-stu-id="a5b04-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="a5b04-112">Los filtros se pueden registrar con valores intermedios no definidos por esta enumeración, como el **mérito \_ normal** + 1.</span><span class="sxs-lookup"><span data-stu-id="a5b04-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b04-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b04-113">Requirements</span></span>



| <span data-ttu-id="a5b04-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b04-114">Requirement</span></span> | <span data-ttu-id="a5b04-115">Value</span><span class="sxs-lookup"><span data-stu-id="a5b04-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b04-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5b04-116">Header</span></span><br/> | <dl> <span data-ttu-id="a5b04-117"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b04-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b04-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5b04-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b04-119">Constantes y GUID</span><span class="sxs-lookup"><span data-stu-id="a5b04-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="a5b04-120">Directrices para registrar filtros</span><span class="sxs-lookup"><span data-stu-id="a5b04-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="a5b04-121">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="a5b04-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




