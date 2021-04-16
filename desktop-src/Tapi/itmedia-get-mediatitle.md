---
description: El \_ método get MediaTitle recupera un título textual para los medios que la aplicación puede usar para fines informativos o de presentación. Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII. De lo contrario, puede ser cualquier cadena BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Método ITMedia:: get_MediaTitle (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680174"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="8bd5d-105">ITMedia:: get \_ MediaTitle (método)</span><span class="sxs-lookup"><span data-stu-id="8bd5d-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="8bd5d-106">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8bd5d-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8bd5d-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8bd5d-108">El método **Get \_ MediaTitle** recupera un título textual para los medios que la aplicación puede usar para fines informativos o de presentación.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="8bd5d-109">Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="8bd5d-110">De lo contrario, puede ser cualquier cadena **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="8bd5d-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd5d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bd5d-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="8bd5d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bd5d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd5d-113">*ppMediaTitle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8bd5d-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd5d-114">Puntero a un **BSTR** que contiene el título del medio.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd5d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bd5d-115">Return value</span></span>

<span data-ttu-id="8bd5d-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="8bd5d-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8bd5d-117">Return code</span></span>                                                                                   | <span data-ttu-id="8bd5d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bd5d-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8bd5d-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8bd5d-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8bd5d-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8bd5d-122">El parámetro *ppMediaTitle* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8bd5d-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8bd5d-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8bd5d-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8bd5d-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8bd5d-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8bd5d-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8bd5d-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8bd5d-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bd5d-129">Remarks</span></span>

<span data-ttu-id="8bd5d-130">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppMediaTitle* .</span><span class="sxs-lookup"><span data-stu-id="8bd5d-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd5d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bd5d-131">Requirements</span></span>



| <span data-ttu-id="8bd5d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bd5d-132">Requirement</span></span> | <span data-ttu-id="8bd5d-133">Value</span><span class="sxs-lookup"><span data-stu-id="8bd5d-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd5d-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8bd5d-134">TAPI version</span></span><br/> | <span data-ttu-id="8bd5d-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8bd5d-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8bd5d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bd5d-136">Header</span></span><br/>       | <dl> <span data-ttu-id="8bd5d-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bd5d-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bd5d-138">Library</span></span><br/>      | <dl> <span data-ttu-id="8bd5d-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8bd5d-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bd5d-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="8bd5d-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd5d-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd5d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bd5d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd5d-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="8bd5d-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="8bd5d-144">**ITMedia::P UT \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="8bd5d-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

