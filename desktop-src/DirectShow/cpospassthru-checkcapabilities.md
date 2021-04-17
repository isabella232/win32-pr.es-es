---
description: 'El método CheckCapabilities consulta si un flujo tiene funcionalidades de búsqueda especificadas. Este método implementa el método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Método CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680474"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="0fc5c-104">CPosPassThru. CheckCapabilities, método</span><span class="sxs-lookup"><span data-stu-id="0fc5c-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="0fc5c-105">El `CheckCapabilities` método consulta si un flujo tiene capacidades de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="0fc5c-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="0fc5c-106">Este método implementa el método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="0fc5c-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc5c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fc5c-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="0fc5c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fc5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc5c-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="0fc5c-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc5c-110">Puntero a una combinación bit a bit de uno o más atributos de [**\_ \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0fc5c-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="0fc5c-111">Cuando el método devuelve, el valor indica cuál de esos atributos está disponible.</span><span class="sxs-lookup"><span data-stu-id="0fc5c-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc5c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fc5c-112">Return value</span></span>

<span data-ttu-id="0fc5c-113">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="0fc5c-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc5c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc5c-114">Requirements</span></span>



| <span data-ttu-id="0fc5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc5c-115">Requirement</span></span> | <span data-ttu-id="0fc5c-116">Value</span><span class="sxs-lookup"><span data-stu-id="0fc5c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc5c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fc5c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0fc5c-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc5c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0fc5c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0fc5c-119">Library</span></span><br/> | <dl> <span data-ttu-id="0fc5c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc5c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc5c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fc5c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc5c-122">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="0fc5c-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




