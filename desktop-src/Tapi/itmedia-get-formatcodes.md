---
description: El \_ método get FormatCodes obtiene la lista de códigos de formato de carga de medios. La variante devuelve una SAFEARRAY de BSTR. Cada BSTR dentro de esa matriz es una cadena de código de formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Método ITMedia:: get_FormatCodes (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680610"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="a0b01-105">ITMedia:: get \_ FormatCodes (método)</span><span class="sxs-lookup"><span data-stu-id="a0b01-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="a0b01-106">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a0b01-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0b01-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a0b01-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0b01-108">El método **Get \_ FormatCodes** obtiene la lista de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="a0b01-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="a0b01-109">La variante devuelve una matriz SAFEARRAY de **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="a0b01-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="a0b01-110">Cada **BSTR** dentro de esa matriz es una cadena de código de formato.</span><span class="sxs-lookup"><span data-stu-id="a0b01-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b01-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0b01-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a0b01-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0b01-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b01-113">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a0b01-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b01-114">Matriz de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="a0b01-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b01-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0b01-115">Return value</span></span>

<span data-ttu-id="a0b01-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a0b01-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a0b01-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a0b01-117">Return code</span></span>                                                                                   | <span data-ttu-id="a0b01-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0b01-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a0b01-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a0b01-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0b01-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a0b01-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a0b01-122">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="a0b01-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="a0b01-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a0b01-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a0b01-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a0b01-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a0b01-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a0b01-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a0b01-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a0b01-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="a0b01-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a0b01-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0b01-129">Remarks</span></span>

<span data-ttu-id="a0b01-130">Cuando se proporciona una lista de formatos de carga, esto implica que todos estos formatos se pueden usar en la sesión, pero el primero de estos formatos es el predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0b01-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="a0b01-131">Cuando el protocolo de transporte es RTP, los códigos de formato son tipos de carga RTP.</span><span class="sxs-lookup"><span data-stu-id="a0b01-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b01-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0b01-132">Requirements</span></span>



| <span data-ttu-id="a0b01-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b01-133">Requirement</span></span> | <span data-ttu-id="a0b01-134">Value</span><span class="sxs-lookup"><span data-stu-id="a0b01-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b01-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a0b01-135">TAPI version</span></span><br/> | <span data-ttu-id="a0b01-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a0b01-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a0b01-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0b01-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a0b01-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0b01-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0b01-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a0b01-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a0b01-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0b01-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a0b01-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b01-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0b01-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b01-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="a0b01-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a0b01-145">**ITMedia::p UT \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="a0b01-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




