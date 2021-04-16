---
description: 'El método GetInfo recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y detención. Este método implementa el método IAMStreamControl:: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Método CBaseStreamControl. GetInfo (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671461"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="0f185-104">CBaseStreamControl. GetInfo (método)</span><span class="sxs-lookup"><span data-stu-id="0f185-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="0f185-105">El `GetInfo` método recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="0f185-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="0f185-106">Este método implementa el método [**IAMStreamControl:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="0f185-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f185-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f185-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0f185-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f185-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="0f185-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0f185-110">Puntero a una estructura de [**\_ \_ información de flujo AM**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , asignada por el llamador, que recibe la configuración de control de flujo actual.</span><span class="sxs-lookup"><span data-stu-id="0f185-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f185-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f185-111">Return value</span></span>

<span data-ttu-id="0f185-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="0f185-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f185-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f185-113">Requirements</span></span>



| <span data-ttu-id="0f185-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f185-114">Requirement</span></span> | <span data-ttu-id="0f185-115">Value</span><span class="sxs-lookup"><span data-stu-id="0f185-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f185-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f185-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0f185-117"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f185-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f185-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f185-118">Library</span></span><br/> | <dl> <span data-ttu-id="0f185-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f185-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f185-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f185-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f185-121">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="0f185-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




