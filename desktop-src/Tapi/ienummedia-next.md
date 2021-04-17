---
description: El método siguiente obtiene el siguiente número de elementos especificado en la secuencia de enumeración.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia:: Next (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681143"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="e5b5f-103">IEnumMedia:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="e5b5f-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="e5b5f-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e5b5f-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e5b5f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e5b5f-106">El método **siguiente** obtiene el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b5f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5b5f-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="e5b5f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5b5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b5f-109">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e5b5f-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b5f-110">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="e5b5f-111">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e5b5f-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b5f-112">Puntero a la interfaz [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b5f-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e5b5f-113">*pceltFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e5b5f-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b5f-114">Puntero al número de elementos proporcionados realmente.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="e5b5f-115">Puede ser **null** si *Celt* es uno.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b5f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5b5f-116">Return value</span></span>

<span data-ttu-id="e5b5f-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e5b5f-118">Value</span><span class="sxs-lookup"><span data-stu-id="e5b5f-118">Value</span></span>                                                                                     | <span data-ttu-id="e5b5f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e5b5f-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="e5b5f-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e5b5f-121">El método devolvió un número de elementos de *Celt* .</span><span class="sxs-lookup"><span data-stu-id="e5b5f-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="e5b5f-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="e5b5f-123">El número de elementos restantes era menor que *Celt*.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="e5b5f-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e5b5f-125">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="e5b5f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5b5f-126">Remarks</span></span>

<span data-ttu-id="e5b5f-127">TAPI llama al método **AddRef** en la interfaz [**ITMedia**](itmedia.md) devuelta por **IEnumMedia:: Next**.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="e5b5f-128">La aplicación debe llamar a **Release** en la interfaz **ITMedia** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b5f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b5f-129">Requirements</span></span>



| <span data-ttu-id="e5b5f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b5f-130">Requirement</span></span> | <span data-ttu-id="e5b5f-131">Value</span><span class="sxs-lookup"><span data-stu-id="e5b5f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b5f-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e5b5f-132">TAPI version</span></span><br/> | <span data-ttu-id="e5b5f-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e5b5f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e5b5f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5b5f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e5b5f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5b5f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5b5f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e5b5f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e5b5f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5b5f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e5b5f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b5f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5b5f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b5f-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="e5b5f-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




