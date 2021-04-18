---
description: Nombre del PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Miembro CBasePin:: m_pName (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661067"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="586a6-103">Miembro pName CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="586a6-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="586a6-104">Nombre del PIN.</span><span class="sxs-lookup"><span data-stu-id="586a6-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="586a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="586a6-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="586a6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="586a6-106">Remarks</span></span>

<span data-ttu-id="586a6-107">El método [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) devuelve esta cadena como el nombre del PIN y el método [**CBasePin:: queryId**](cbasepin-queryid.md) la devuelve como identificador de PIN.</span><span class="sxs-lookup"><span data-stu-id="586a6-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="586a6-108">Sin embargo, en general, el nombre del PIN y el identificador del PIN no deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="586a6-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="586a6-109">El identificador del PIN se usa para la persistencia del gráfico.</span><span class="sxs-lookup"><span data-stu-id="586a6-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="586a6-110">Para obtener más información, vea [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="586a6-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="586a6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="586a6-111">Requirements</span></span>



| <span data-ttu-id="586a6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="586a6-112">Requirement</span></span> | <span data-ttu-id="586a6-113">Value</span><span class="sxs-lookup"><span data-stu-id="586a6-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586a6-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="586a6-114">Header</span></span><br/> | <dl> <span data-ttu-id="586a6-115"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="586a6-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586a6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="586a6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586a6-117">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="586a6-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




