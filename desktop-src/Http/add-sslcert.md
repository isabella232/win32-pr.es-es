---
title: add sslcert
description: Agrega un nuevo enlace de certificado de servidor Capa de sockets seguros (SSL) y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Agregar sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a43569edd400b824876dff991f95e79cbfd6a96
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419787"
---
# <a name="add-sslcert"></a><span data-ttu-id="e5e37-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="e5e37-104">add sslcert</span></span>

<span data-ttu-id="e5e37-105">Agrega un nuevo enlace de certificado de servidor Capa de sockets seguros (SSL) y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.</span><span class="sxs-lookup"><span data-stu-id="e5e37-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="e5e37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e37-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* dirección IP: Puerto*</span><span class="sxs-lookup"><span data-stu-id="e5e37-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-108">Especifica la dirección IP y el puerto para el enlace.</span><span class="sxs-lookup"><span data-stu-id="e5e37-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[certhash = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="e5e37-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[certhash=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-110">Especifica el hash SHA del certificado.</span><span class="sxs-lookup"><span data-stu-id="e5e37-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="e5e37-111">Este hash tiene una longitud de 20 bytes y se especifica como una cadena hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e5e37-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[AppID = \] \* \* \* GUID*</span><span class="sxs-lookup"><span data-stu-id="e5e37-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[appid=\]\*\*\*GUID*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-113">Especifica el GUID para identificar la aplicación propietaria.</span><span class="sxs-lookup"><span data-stu-id="e5e37-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[certstorename = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="e5e37-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[certstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-115">Especifica el nombre del almacén del certificado.</span><span class="sxs-lookup"><span data-stu-id="e5e37-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="e5e37-116">El valor predeterminado es MY.</span><span class="sxs-lookup"><span data-stu-id="e5e37-116">Defaults to MY.</span></span> <span data-ttu-id="e5e37-117">El certificado debe almacenarse en el contexto del equipo local.</span><span class="sxs-lookup"><span data-stu-id="e5e37-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {enable \| Disable}\]**</span><span class="sxs-lookup"><span data-stu-id="e5e37-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-119">Activa o turnsoff la comprobación de la revocación de certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="e5e37-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {enable \| Disable}\]**</span><span class="sxs-lookup"><span data-stu-id="e5e37-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-121">Activa o desactiva el uso del certificado de cliente almacenado en caché únicamente para la comprobación de revocación.</span><span class="sxs-lookup"><span data-stu-id="e5e37-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {enable \| Disable}\]**</span><span class="sxs-lookup"><span data-stu-id="e5e37-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-123">Activa o desactiva la comprobación de uso.</span><span class="sxs-lookup"><span data-stu-id="e5e37-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="e5e37-124">Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e5e37-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[RevocationFreshnessTime = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="e5e37-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[revocationfreshnesstime=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-126">Especifica el intervalo de tiempo para comprobar una lista de revocación de certificados (CRL) actualizada.</span><span class="sxs-lookup"><span data-stu-id="e5e37-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="e5e37-127">Si este valor es 0, la nueva CRL solo se actualiza si la anterior expira (en segundos).</span><span class="sxs-lookup"><span data-stu-id="e5e37-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[urlretrievaltimeout = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="e5e37-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[urlretrievaltimeout=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-129">Especifica el intervalo de tiempo de espera de los intentos de recuperar la lista de revocación de certificados para la dirección URL remota (en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="e5e37-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[sslctlidentifier = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="e5e37-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[sslctlidentifier=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-131">Enumera los emisores de certificados en los que se puede confiar.</span><span class="sxs-lookup"><span data-stu-id="e5e37-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="e5e37-132">Esta lista puede ser un subconjunto de los emisores de certificados que son de confianza para el equipo.</span><span class="sxs-lookup"><span data-stu-id="e5e37-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[SslCtlStoreName = \] \* \* \* cadena*</span><span class="sxs-lookup"><span data-stu-id="e5e37-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[sslctlstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-134">Especifica el nombre del almacén en el \_ equipo local donde se almacena SslCtlIdentifier.</span><span class="sxs-lookup"><span data-stu-id="e5e37-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {enable \| Disable}\]**</span><span class="sxs-lookup"><span data-stu-id="e5e37-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-136">Activa o desactiva los asignadores de DS.</span><span class="sxs-lookup"><span data-stu-id="e5e37-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="e5e37-137">De forma predeterminada, está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e5e37-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e5e37-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {enable \| Disable}\]**</span><span class="sxs-lookup"><span data-stu-id="e5e37-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="e5e37-139">Activa o desactiva la negociación del certificado.</span><span class="sxs-lookup"><span data-stu-id="e5e37-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="e5e37-140">De forma predeterminada, está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e5e37-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e5e37-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e5e37-141">Examples</span></span>

<span data-ttu-id="e5e37-142">**Add sslcert ipport = pág: 443**</span><span class="sxs-lookup"><span data-stu-id="e5e37-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="e5e37-143">**certhash = 0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="e5e37-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="e5e37-144">**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="e5e37-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




