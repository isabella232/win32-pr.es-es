---
description: El \_ método get URL obtiene la dirección URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'Método ITSdp:: get_Url (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681296"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="68f60-103">ITSdp:: get \_ URL (método)</span><span class="sxs-lookup"><span data-stu-id="68f60-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="68f60-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68f60-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68f60-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="68f60-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68f60-106">El método **Get \_ URL** obtiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="68f60-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f60-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68f60-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="68f60-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68f60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f60-109">*ppUrl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68f60-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f60-110">Puntero a una representación **BSTR** de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="68f60-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f60-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68f60-111">Return value</span></span>

<span data-ttu-id="68f60-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="68f60-112">This method can return one of these values.</span></span>



| <span data-ttu-id="68f60-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68f60-113">Return code</span></span>                                                                                   | <span data-ttu-id="68f60-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="68f60-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="68f60-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68f60-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="68f60-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="68f60-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68f60-118">El parámetro *ppUrl* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="68f60-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="68f60-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68f60-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="68f60-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="68f60-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="68f60-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="68f60-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="68f60-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="68f60-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="68f60-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="68f60-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68f60-125">Remarks</span></span>

<span data-ttu-id="68f60-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppUrl* .</span><span class="sxs-lookup"><span data-stu-id="68f60-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="68f60-127">Una dirección URL se usa normalmente para hacer referencia a una página web que contiene recursos adicionales o información general sobre una conferencia.</span><span class="sxs-lookup"><span data-stu-id="68f60-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f60-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68f60-128">Requirements</span></span>



| <span data-ttu-id="68f60-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="68f60-129">Requirement</span></span> | <span data-ttu-id="68f60-130">Value</span><span class="sxs-lookup"><span data-stu-id="68f60-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68f60-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="68f60-131">TAPI version</span></span><br/> | <span data-ttu-id="68f60-132">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="68f60-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="68f60-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68f60-133">Header</span></span><br/>       | <dl> <span data-ttu-id="68f60-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="68f60-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68f60-135">Library</span></span><br/>      | <dl> <span data-ttu-id="68f60-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="68f60-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68f60-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="68f60-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f60-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f60-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="68f60-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f60-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="68f60-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="68f60-141">**ITSdp::p \_ dirección URL de UT**</span><span class="sxs-lookup"><span data-stu-id="68f60-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

