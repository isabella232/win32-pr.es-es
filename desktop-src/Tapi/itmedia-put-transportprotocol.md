---
description: El \_ método put TransportProtocol establece el protocolo de transporte.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'ITMedia: método de ut_TransportProtocol de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680321"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="7e10a-103">ITMedia::p \_ método TransportProtocol UT</span><span class="sxs-lookup"><span data-stu-id="7e10a-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="7e10a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7e10a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e10a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7e10a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e10a-106">El método **Put \_ TransportProtocol** establece el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e10a-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="7e10a-107">Esto se especifica además del formato de medios, de modo que se pueda trasladar el mismo formato multimedia estándar a los diferentes protocolos de transporte, incluso cuando el protocolo de red sea el mismo, por ejemplo, con el audio del PCM de IVA y el audio del PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="7e10a-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e10a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e10a-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7e10a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e10a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e10a-110">*pProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e10a-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e10a-111">Puntero a un **BSTR** que contiene el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e10a-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e10a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e10a-112">Return value</span></span>

<span data-ttu-id="7e10a-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7e10a-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7e10a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7e10a-114">Return code</span></span>                                                                                   | <span data-ttu-id="7e10a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e10a-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7e10a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7e10a-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e10a-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7e10a-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7e10a-119">El parámetro *pProtocol* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="7e10a-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="7e10a-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7e10a-121">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="7e10a-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7e10a-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7e10a-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7e10a-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7e10a-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7e10a-125">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="7e10a-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7e10a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e10a-126">Remarks</span></span>

<span data-ttu-id="7e10a-127">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PProtocol* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="7e10a-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="7e10a-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="7e10a-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="7e10a-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="7e10a-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e10a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e10a-130">Requirements</span></span>



| <span data-ttu-id="7e10a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e10a-131">Requirement</span></span> | <span data-ttu-id="7e10a-132">Value</span><span class="sxs-lookup"><span data-stu-id="7e10a-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e10a-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7e10a-133">TAPI version</span></span><br/> | <span data-ttu-id="7e10a-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7e10a-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7e10a-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e10a-135">Header</span></span><br/>       | <dl> <span data-ttu-id="7e10a-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e10a-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e10a-137">Library</span></span><br/>      | <dl> <span data-ttu-id="7e10a-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7e10a-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e10a-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="7e10a-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e10a-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e10a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e10a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e10a-142">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="7e10a-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="7e10a-143">**ITMedia:: get \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="7e10a-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

