---
description: El \_ método get Name obtiene el nombre de la sesión.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'Método ITSdp:: get_Name (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679153"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="f42aa-103">ITSdp:: get \_ Name (método)</span><span class="sxs-lookup"><span data-stu-id="f42aa-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="f42aa-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f42aa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f42aa-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f42aa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f42aa-106">El método **Get \_ Name** obtiene el nombre de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f42aa-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="f42aa-107">Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII.</span><span class="sxs-lookup"><span data-stu-id="f42aa-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="f42aa-108">(De lo contrario, puede ser cualquier cadena **BSTR** ).</span><span class="sxs-lookup"><span data-stu-id="f42aa-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="f42aa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f42aa-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="f42aa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f42aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42aa-111">*ppName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f42aa-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f42aa-112">Puntero a un **BSTR** que contiene el nombre de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f42aa-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42aa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f42aa-113">Return value</span></span>

<span data-ttu-id="f42aa-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f42aa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f42aa-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f42aa-115">Return code</span></span>                                                                                   | <span data-ttu-id="f42aa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f42aa-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f42aa-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f42aa-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f42aa-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f42aa-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f42aa-120">El parámetro *ppName* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f42aa-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="f42aa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f42aa-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f42aa-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f42aa-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f42aa-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f42aa-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f42aa-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f42aa-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f42aa-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f42aa-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f42aa-127">Remarks</span></span>

<span data-ttu-id="f42aa-128">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppName* .</span><span class="sxs-lookup"><span data-stu-id="f42aa-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42aa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f42aa-129">Requirements</span></span>



| <span data-ttu-id="f42aa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f42aa-130">Requirement</span></span> | <span data-ttu-id="f42aa-131">Value</span><span class="sxs-lookup"><span data-stu-id="f42aa-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f42aa-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f42aa-132">TAPI version</span></span><br/> | <span data-ttu-id="f42aa-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f42aa-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f42aa-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f42aa-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f42aa-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f42aa-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f42aa-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f42aa-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f42aa-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f42aa-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f42aa-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f42aa-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42aa-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f42aa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f42aa-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f42aa-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f42aa-142">**ITSdp::p nombre de UT \_**</span><span class="sxs-lookup"><span data-stu-id="f42aa-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

