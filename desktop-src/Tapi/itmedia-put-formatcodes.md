---
description: El \_ método put FormatCodes establece la lista de códigos de formato de carga de medios. La variante contiene una SAFEARRAY de BSTR. Cada BSTR dentro de esa matriz es una cadena de código de formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: método de ut_FormatCodes de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689906"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="0b278-105">ITMedia::p \_ método FormatCodes UT</span><span class="sxs-lookup"><span data-stu-id="0b278-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="0b278-106">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b278-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0b278-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0b278-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0b278-108">El método **Put \_ FormatCodes** establece la lista de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="0b278-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="0b278-109">La variante contiene una SAFEARRAY de **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="0b278-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="0b278-110">Cada **BSTR** dentro de esa matriz es una cadena de código de formato.</span><span class="sxs-lookup"><span data-stu-id="0b278-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b278-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b278-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="0b278-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b278-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b278-113">*NewVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b278-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b278-114">Lista de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="0b278-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b278-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b278-115">Return value</span></span>

<span data-ttu-id="0b278-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0b278-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0b278-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0b278-117">Return code</span></span>                                                                                   | <span data-ttu-id="0b278-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b278-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0b278-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b278-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b278-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0b278-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0b278-122">El parámetro *NewVal* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0b278-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="0b278-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b278-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0b278-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0b278-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0b278-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0b278-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0b278-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0b278-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="0b278-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0b278-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b278-129">Remarks</span></span>

<span data-ttu-id="0b278-130">Cuando se proporciona una lista de formatos de carga, esto implica que todos estos formatos se pueden usar en la sesión, pero el primero de estos formatos es el predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="0b278-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="0b278-131">Cuando el protocolo de transporte es RTP, los códigos de formato son tipos de carga RTP.</span><span class="sxs-lookup"><span data-stu-id="0b278-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b278-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b278-132">Requirements</span></span>



| <span data-ttu-id="0b278-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b278-133">Requirement</span></span> | <span data-ttu-id="0b278-134">Value</span><span class="sxs-lookup"><span data-stu-id="0b278-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b278-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0b278-135">TAPI version</span></span><br/> | <span data-ttu-id="0b278-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0b278-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0b278-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b278-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0b278-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b278-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b278-139">Library</span></span><br/>      | <dl> <span data-ttu-id="0b278-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0b278-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b278-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="0b278-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b278-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b278-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b278-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b278-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="0b278-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="0b278-145">**ITMedia:: get \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="0b278-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




