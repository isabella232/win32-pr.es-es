---
description: 'Método IEnumTime::Next: el método Next obtiene el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: Método IEnumTime::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118393"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="dc7e4-103">IEnumTime::Next (método)</span><span class="sxs-lookup"><span data-stu-id="dc7e4-103">IEnumTime::Next method</span></span>

<span data-ttu-id="dc7e4-104">\[ Los controles e interfaces de Conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc7e4-105">La API de cliente RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="dc7e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dc7e4-106">El **método Next** obtiene el siguiente número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc7e4-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="dc7e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc7e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7e4-109">*celta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dc7e4-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7e4-110">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="dc7e4-111">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc7e4-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7e4-112">Puntero a la [**interfaz ITTime.**](ittime.md)</span><span class="sxs-lookup"><span data-stu-id="dc7e4-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dc7e4-113">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc7e4-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7e4-114">Puntero al número de elementos proporcionados realmente.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="dc7e4-115">Puede ser **NULL** si *celt* es 1.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7e4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7e4-116">Return value</span></span>

<span data-ttu-id="dc7e4-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-117">This method can return one of these values.</span></span>



| <span data-ttu-id="dc7e4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dc7e4-118">Value</span></span>                                                                                     | <span data-ttu-id="dc7e4-119">Significado</span><span class="sxs-lookup"><span data-stu-id="dc7e4-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="dc7e4-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="dc7e4-121">El método *devolvió el número* de celtas de elementos.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="dc7e4-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="dc7e4-123">El número de elementos restantes era menor *que celta.*</span><span class="sxs-lookup"><span data-stu-id="dc7e4-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="dc7e4-124"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="dc7e4-125">El *parámetro pVal* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="dc7e4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc7e4-126">Remarks</span></span>

<span data-ttu-id="dc7e4-127">TAPI llama al **método AddRef** en la [**interfaz ITTime**](ittime.md) devuelta por **IEnumTime::Next**.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="dc7e4-128">La aplicación debe llamar a **Release en** la **interfaz ITTime** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="dc7e4-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7e4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc7e4-129">Requirements</span></span>



| <span data-ttu-id="dc7e4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc7e4-130">Requirement</span></span> | <span data-ttu-id="dc7e4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="dc7e4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7e4-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="dc7e4-132">TAPI version</span></span><br/> | <span data-ttu-id="dc7e4-133">Requiere TAPI 3.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dc7e4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dc7e4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc7e4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="dc7e4-135"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc7e4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc7e4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="dc7e4-137"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dc7e4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc7e4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="dc7e4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc7e4-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc7e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7e4-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="dc7e4-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




