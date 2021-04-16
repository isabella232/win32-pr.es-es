---
title: IMsTscAxEvents método OnDisconnect
description: Se llama cuando el control de cliente se ha desconectado del servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Método OnDisconnection Servicios de Escritorio remoto
- Método OnDisconnection Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnDisconnect
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676820"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="37be1-106">IMsTscAxEvents:: OnDisconnection (método)</span><span class="sxs-lookup"><span data-stu-id="37be1-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="37be1-107">Se llama cuando el control de cliente se ha desconectado del servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="37be1-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="37be1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37be1-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="37be1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37be1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37be1-110">*discReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37be1-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37be1-111">Especifica el motivo de la desconexión.</span><span class="sxs-lookup"><span data-stu-id="37be1-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="37be1-112">A continuación se muestra una lista de códigos de error.</span><span class="sxs-lookup"><span data-stu-id="37be1-112">The following is a list of error codes.</span></span> <span data-ttu-id="37be1-113">Algunos de estos códigos de error se definen en Wincred. h.</span><span class="sxs-lookup"><span data-stu-id="37be1-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="37be1-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span><span class="sxs-lookup"><span data-stu-id="37be1-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-115">Socket cerrado.</span><span class="sxs-lookup"><span data-stu-id="37be1-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="37be1-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="37be1-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-117">Desconexión remota por servidor.</span><span class="sxs-lookup"><span data-stu-id="37be1-117">Remote disconnection by server.</span></span> <span data-ttu-id="37be1-118">No es un código de error.</span><span class="sxs-lookup"><span data-stu-id="37be1-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="37be1-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span><span class="sxs-lookup"><span data-stu-id="37be1-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-120">Error de descompresión.</span><span class="sxs-lookup"><span data-stu-id="37be1-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="37be1-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span><span class="sxs-lookup"><span data-stu-id="37be1-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-122">La conexión ha agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="37be1-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="37be1-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span><span class="sxs-lookup"><span data-stu-id="37be1-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-124">Error de descifrado.</span><span class="sxs-lookup"><span data-stu-id="37be1-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="37be1-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span><span class="sxs-lookup"><span data-stu-id="37be1-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-126">Error de búsqueda de nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="37be1-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="37be1-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span><span class="sxs-lookup"><span data-stu-id="37be1-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-128">Error de búsqueda de DNS.</span><span class="sxs-lookup"><span data-stu-id="37be1-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="37be1-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span><span class="sxs-lookup"><span data-stu-id="37be1-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-130">Error de cifrado.</span><span class="sxs-lookup"><span data-stu-id="37be1-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="37be1-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span><span class="sxs-lookup"><span data-stu-id="37be1-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-132">Error en la llamada [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="37be1-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="37be1-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span><span class="sxs-lookup"><span data-stu-id="37be1-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-134">Error de host no encontrado.</span><span class="sxs-lookup"><span data-stu-id="37be1-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="37be1-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span><span class="sxs-lookup"><span data-stu-id="37be1-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-136">Error interno.</span><span class="sxs-lookup"><span data-stu-id="37be1-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="37be1-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span><span class="sxs-lookup"><span data-stu-id="37be1-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-138">Error de seguridad interno.</span><span class="sxs-lookup"><span data-stu-id="37be1-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="37be1-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span><span class="sxs-lookup"><span data-stu-id="37be1-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-140">Error de seguridad interno.</span><span class="sxs-lookup"><span data-stu-id="37be1-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="37be1-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span><span class="sxs-lookup"><span data-stu-id="37be1-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-142">El método de cifrado especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="37be1-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="37be1-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span><span class="sxs-lookup"><span data-stu-id="37be1-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-144">Se especificó una dirección IP incorrecta.</span><span class="sxs-lookup"><span data-stu-id="37be1-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="37be1-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span><span class="sxs-lookup"><span data-stu-id="37be1-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-146">Los datos de seguridad del servidor no son válidos.</span><span class="sxs-lookup"><span data-stu-id="37be1-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="37be1-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span><span class="sxs-lookup"><span data-stu-id="37be1-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-148">Los datos de seguridad no son válidos.</span><span class="sxs-lookup"><span data-stu-id="37be1-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="37be1-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span><span class="sxs-lookup"><span data-stu-id="37be1-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-150">La dirección IP especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="37be1-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="37be1-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span><span class="sxs-lookup"><span data-stu-id="37be1-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-152">Error de negociación de licencia.</span><span class="sxs-lookup"><span data-stu-id="37be1-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="37be1-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span><span class="sxs-lookup"><span data-stu-id="37be1-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-154">Tiempo de espera de licencia.</span><span class="sxs-lookup"><span data-stu-id="37be1-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="37be1-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="37be1-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-156">Desconexión local.</span><span class="sxs-lookup"><span data-stu-id="37be1-156">Local disconnection.</span></span> <span data-ttu-id="37be1-157">No es un código de error.</span><span class="sxs-lookup"><span data-stu-id="37be1-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="37be1-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="37be1-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-159">No hay información disponible.</span><span class="sxs-lookup"><span data-stu-id="37be1-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="37be1-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span><span class="sxs-lookup"><span data-stu-id="37be1-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-161">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="37be1-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="37be1-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span><span class="sxs-lookup"><span data-stu-id="37be1-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-163">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="37be1-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="37be1-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span><span class="sxs-lookup"><span data-stu-id="37be1-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-165">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="37be1-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="37be1-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="37be1-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-167">Desconexión remota por usuario.</span><span class="sxs-lookup"><span data-stu-id="37be1-167">Remote disconnection by user.</span></span> <span data-ttu-id="37be1-168">No es un código de error.</span><span class="sxs-lookup"><span data-stu-id="37be1-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="37be1-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span><span class="sxs-lookup"><span data-stu-id="37be1-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-170">No se pudo desempaquetar el certificado de servidor.</span><span class="sxs-lookup"><span data-stu-id="37be1-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="37be1-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span><span class="sxs-lookup"><span data-stu-id="37be1-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-172">Error de conexión de Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .</span><span class="sxs-lookup"><span data-stu-id="37be1-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="37be1-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span><span class="sxs-lookup"><span data-stu-id="37be1-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-174">Error en la llamada de [**recepción**](/windows/desktop/api/winsock/nf-winsock-recv) de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="37be1-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="37be1-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span><span class="sxs-lookup"><span data-stu-id="37be1-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-176">Se agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="37be1-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="37be1-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span><span class="sxs-lookup"><span data-stu-id="37be1-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-178">Error de temporizador interno.</span><span class="sxs-lookup"><span data-stu-id="37be1-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="37be1-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span><span class="sxs-lookup"><span data-stu-id="37be1-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-180">Error en la llamada de [**envío**](/windows/desktop/api/winsock2/nf-winsock2-send) de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="37be1-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="37be1-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_ de Cuenta de ERR \_ \_ deshabilitada** (2823 (0xB07))</span><span class="sxs-lookup"><span data-stu-id="37be1-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-182">La cuenta está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="37be1-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="37be1-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_ de Cuenta de ERR \_ \_ expirada** (3591 (0xE07))</span><span class="sxs-lookup"><span data-stu-id="37be1-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-184">La cuenta ha expirado.</span><span class="sxs-lookup"><span data-stu-id="37be1-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="37be1-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_ de Cuenta de ERR \_ \_ bloqueada \_** (3335 (0xD07))</span><span class="sxs-lookup"><span data-stu-id="37be1-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-186">Se ha bloqueado la cuenta.</span><span class="sxs-lookup"><span data-stu-id="37be1-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="37be1-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_ de \_ \_ Restricción** de la cuenta de ERR (3079 (0xC07))</span><span class="sxs-lookup"><span data-stu-id="37be1-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-188">La cuenta está restringida.</span><span class="sxs-lookup"><span data-stu-id="37be1-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="37be1-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ de ERR \_ CERT \_ Expired** (6919 (0x1B07))</span><span class="sxs-lookup"><span data-stu-id="37be1-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-190">El certificado recibido expiró.</span><span class="sxs-lookup"><span data-stu-id="37be1-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="37be1-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_ de \_ \_ Directiva de delegación de ERR** (5639) (0x1607)</span><span class="sxs-lookup"><span data-stu-id="37be1-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-192">La Directiva no admite la delegación de credenciales en el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="37be1-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="37be1-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_ de ERROR \_ \_ de credenciales actualizadas \_ solicitadas \_ por el \_ servidor** (8455 (0x2107))</span><span class="sxs-lookup"><span data-stu-id="37be1-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-194">La Directiva de autenticación de servidor no permite solicitudes de conexión con credenciales guardadas.</span><span class="sxs-lookup"><span data-stu-id="37be1-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="37be1-195">El usuario debe escribir nuevas credenciales.</span><span class="sxs-lookup"><span data-stu-id="37be1-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="37be1-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_ de \_ \_ Error de inicio de sesión** de error (2055) (0x807)</span><span class="sxs-lookup"><span data-stu-id="37be1-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-197">Error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="37be1-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="37be1-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_ de NO se pudo \_ \_ autenticar la \_ entidad de autenticación** (6151 (0x1807))</span><span class="sxs-lookup"><span data-stu-id="37be1-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-199">No se pudo establecer contacto con ninguna autoridad para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="37be1-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="37be1-200">El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría estar inaccesible o podría haber un error de relación de confianza.</span><span class="sxs-lookup"><span data-stu-id="37be1-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="37be1-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_ de NO se ha podido \_ \_ este \_ usuario** (2567 (0xA07))</span><span class="sxs-lookup"><span data-stu-id="37be1-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-202">El usuario especificado no tiene ninguna cuenta.</span><span class="sxs-lookup"><span data-stu-id="37be1-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="37be1-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_ de Contraseña de error \_ \_ expirada** (3847 (0xF07))</span><span class="sxs-lookup"><span data-stu-id="37be1-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-204">La contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="37be1-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="37be1-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_ de La \_ contraseña de Err \_ debe \_ cambiar** (4615 (0x1207))</span><span class="sxs-lookup"><span data-stu-id="37be1-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-206">Se debe cambiar la contraseña del usuario antes de iniciar sesión por primera vez.</span><span class="sxs-lookup"><span data-stu-id="37be1-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="37be1-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ de \_Directiva de \_ Err \_ solo NTLM** (5895 (0x1707))</span><span class="sxs-lookup"><span data-stu-id="37be1-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-208">No se permite la delegación de credenciales en el servidor de destino a menos que se haya logrado la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="37be1-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="37be1-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_ de \_Tarjeta inteligente de error \_ \_ bloqueada** (8711 (0x2207))</span><span class="sxs-lookup"><span data-stu-id="37be1-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-210">La tarjeta inteligente está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="37be1-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="37be1-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_ de PIN de error de \_ tarjeta inteligente \_ errónea \_** (7175 (0x1C07))</span><span class="sxs-lookup"><span data-stu-id="37be1-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="37be1-212">Se presentó un PIN incorrecto a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="37be1-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37be1-213">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37be1-213">Return value</span></span>

<span data-ttu-id="37be1-214">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="37be1-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37be1-215">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37be1-215">Remarks</span></span>

<span data-ttu-id="37be1-216">Para recuperar una descripción del error de desconexión, llame al método [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) y pásele el parámetro *discReason* y la propiedad [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) de la interfaz [**IMsRdpClient**](imsrdpclient-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="37be1-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="37be1-217">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="37be1-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37be1-218">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37be1-218">Requirements</span></span>



| <span data-ttu-id="37be1-219">Requisito</span><span class="sxs-lookup"><span data-stu-id="37be1-219">Requirement</span></span> | <span data-ttu-id="37be1-220">Value</span><span class="sxs-lookup"><span data-stu-id="37be1-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37be1-221">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37be1-221">Minimum supported client</span></span><br/> | <span data-ttu-id="37be1-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37be1-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="37be1-223">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37be1-223">Minimum supported server</span></span><br/> | <span data-ttu-id="37be1-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37be1-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="37be1-225">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="37be1-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="37be1-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37be1-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="37be1-227">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37be1-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37be1-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37be1-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="37be1-229">IID</span><span class="sxs-lookup"><span data-stu-id="37be1-229">IID</span></span><br/>                      | <span data-ttu-id="37be1-230">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="37be1-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="37be1-231">Vea también</span><span class="sxs-lookup"><span data-stu-id="37be1-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37be1-232">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="37be1-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

