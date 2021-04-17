---
description: El \_ método get ConferenceBlob obtiene un puntero al BLOB de la Conferencia textual actualmente almacenado en el objeto de BLOB de la Conferencia.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Método ITConferenceBlob:: get_ConferenceBlob (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680207"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="0973e-103">ITConferenceBlob:: get \_ ConferenceBlob (método)</span><span class="sxs-lookup"><span data-stu-id="0973e-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="0973e-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0973e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0973e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0973e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0973e-106">El método **Get \_ ConferenceBlob** obtiene un puntero al BLOB de la Conferencia textual actualmente almacenado en el objeto de BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0973e-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0973e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0973e-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0973e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0973e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0973e-109">*ppBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0973e-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0973e-110">Puntero a un **BSTR** que contiene el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="0973e-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0973e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0973e-111">Return value</span></span>

<span data-ttu-id="0973e-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0973e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0973e-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0973e-113">Return code</span></span>                                                                                   | <span data-ttu-id="0973e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0973e-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0973e-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0973e-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0973e-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0973e-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0973e-118">El parámetro *ppBlob* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="0973e-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="0973e-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0973e-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0973e-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0973e-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0973e-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0973e-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0973e-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0973e-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="0973e-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0973e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0973e-125">Remarks</span></span>

<span data-ttu-id="0973e-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppBlob* .</span><span class="sxs-lookup"><span data-stu-id="0973e-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0973e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0973e-127">Requirements</span></span>



| <span data-ttu-id="0973e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0973e-128">Requirement</span></span> | <span data-ttu-id="0973e-129">Value</span><span class="sxs-lookup"><span data-stu-id="0973e-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0973e-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0973e-130">TAPI version</span></span><br/> | <span data-ttu-id="0973e-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0973e-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0973e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0973e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0973e-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0973e-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0973e-134">Library</span></span><br/>      | <dl> <span data-ttu-id="0973e-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0973e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0973e-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="0973e-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0973e-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0973e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0973e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0973e-139">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="0973e-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="0973e-140">**\_juego de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="0973e-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

