---
description: El \_ método get TransportProtocol obtiene el protocolo de transporte.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Método ITMedia:: get_TransportProtocol (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678992"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="c948e-103">ITMedia:: get \_ TransportProtocol (método)</span><span class="sxs-lookup"><span data-stu-id="c948e-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="c948e-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c948e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c948e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c948e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c948e-106">El método **Get \_ TransportProtocol** obtiene el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="c948e-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="c948e-107">Esto se especifica además del formato de medios, de modo que se pueda trasladar el mismo formato multimedia estándar a los diferentes protocolos de transporte, incluso cuando el protocolo de red sea el mismo, por ejemplo, con el audio del PCM de IVA y el audio del PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="c948e-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="c948e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c948e-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="c948e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c948e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c948e-110">*ppProtocol* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c948e-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c948e-111">Puntero a la representación **BSTR** del Protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="c948e-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c948e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c948e-112">Return value</span></span>

<span data-ttu-id="c948e-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c948e-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c948e-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c948e-114">Return code</span></span>                                                                                   | <span data-ttu-id="c948e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c948e-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c948e-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c948e-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c948e-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c948e-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c948e-119">El parámetro *ppProtocol* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="c948e-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="c948e-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c948e-121">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c948e-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c948e-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c948e-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c948e-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c948e-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c948e-125">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="c948e-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c948e-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c948e-126">Remarks</span></span>

<span data-ttu-id="c948e-127">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppProtocol* .</span><span class="sxs-lookup"><span data-stu-id="c948e-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c948e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c948e-128">Requirements</span></span>



| <span data-ttu-id="c948e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c948e-129">Requirement</span></span> | <span data-ttu-id="c948e-130">Value</span><span class="sxs-lookup"><span data-stu-id="c948e-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c948e-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c948e-131">TAPI version</span></span><br/> | <span data-ttu-id="c948e-132">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c948e-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c948e-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c948e-133">Header</span></span><br/>       | <dl> <span data-ttu-id="c948e-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c948e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c948e-135">Library</span></span><br/>      | <dl> <span data-ttu-id="c948e-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c948e-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c948e-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="c948e-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c948e-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c948e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c948e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c948e-140">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="c948e-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="c948e-141">**ITMedia::p UT \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="c948e-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

