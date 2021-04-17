---
description: El \_ método put URL establece la dirección URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: 'ITSdp: método de ut_Url de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680452"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="54fc4-103">ITSdp::p \_ método URL de UT</span><span class="sxs-lookup"><span data-stu-id="54fc4-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="54fc4-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="54fc4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="54fc4-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="54fc4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="54fc4-106">El método **Put \_ URL** establece la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="54fc4-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fc4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54fc4-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="54fc4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54fc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54fc4-109">*pUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54fc4-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54fc4-110">Puntero a una representación **BSTR** de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="54fc4-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54fc4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54fc4-111">Return value</span></span>

<span data-ttu-id="54fc4-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="54fc4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="54fc4-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="54fc4-113">Return code</span></span>                                                                                   | <span data-ttu-id="54fc4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="54fc4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="54fc4-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="54fc4-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="54fc4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="54fc4-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="54fc4-118">El parámetro *pUrl* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="54fc4-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="54fc4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="54fc4-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="54fc4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="54fc4-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="54fc4-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="54fc4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="54fc4-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="54fc4-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="54fc4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="54fc4-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54fc4-125">Remarks</span></span>

<span data-ttu-id="54fc4-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PUrl* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="54fc4-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="54fc4-127">Una dirección URL se usa normalmente para hacer referencia a una página web que contiene recursos adicionales o información general sobre una conferencia.</span><span class="sxs-lookup"><span data-stu-id="54fc4-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="54fc4-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="54fc4-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="54fc4-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="54fc4-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="54fc4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54fc4-130">Requirements</span></span>



| <span data-ttu-id="54fc4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="54fc4-131">Requirement</span></span> | <span data-ttu-id="54fc4-132">Value</span><span class="sxs-lookup"><span data-stu-id="54fc4-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54fc4-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="54fc4-133">TAPI version</span></span><br/> | <span data-ttu-id="54fc4-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="54fc4-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="54fc4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54fc4-135">Header</span></span><br/>       | <dl> <span data-ttu-id="54fc4-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="54fc4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54fc4-137">Library</span></span><br/>      | <dl> <span data-ttu-id="54fc4-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="54fc4-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54fc4-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="54fc4-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54fc4-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54fc4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="54fc4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fc4-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="54fc4-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="54fc4-143">**ITSdp:: get \_ URL**</span><span class="sxs-lookup"><span data-stu-id="54fc4-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

