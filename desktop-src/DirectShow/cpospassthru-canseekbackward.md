---
description: 'El método CanSeekBackward determina si la secuencia se puede buscar hacia atrás. Este método implementa el método IMediaPosition:: CanSeekBackward.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Método CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679170"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="ca2e6-104">CPosPassThru. CanSeekBackward, método</span><span class="sxs-lookup"><span data-stu-id="ca2e6-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="ca2e6-105">El `CanSeekBackward` método determina si la secuencia se puede buscar hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="ca2e6-106">Este método implementa el método [**IMediaPosition:: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .</span><span class="sxs-lookup"><span data-stu-id="ca2e6-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2e6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca2e6-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="ca2e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca2e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2e6-109">*pCanSeekBackward*</span><span class="sxs-lookup"><span data-stu-id="ca2e6-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="ca2e6-110">Puntero a una variable que recibe el valor OATRUE si el filtro puede buscar hacia atrás o OAFALSE de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2e6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca2e6-111">Return value</span></span>

<span data-ttu-id="ca2e6-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2e6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca2e6-113">Requirements</span></span>



| <span data-ttu-id="ca2e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca2e6-114">Requirement</span></span> | <span data-ttu-id="ca2e6-115">Value</span><span class="sxs-lookup"><span data-stu-id="ca2e6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2e6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca2e6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ca2e6-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca2e6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca2e6-118">Library</span></span><br/> | <dl> <span data-ttu-id="ca2e6-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2e6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca2e6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2e6-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




