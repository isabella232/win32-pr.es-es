---
title: add sslcert
description: Agrega un nuevo enlace Capa de sockets seguros de certificado de servidor (SSL) y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- add sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644197"
---
# <a name="add-sslcert"></a><span data-ttu-id="71575-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="71575-104">add sslcert</span></span>

<span data-ttu-id="71575-105">Agrega un nuevo enlace Capa de sockets seguros de certificado de servidor (SSL) y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.</span><span class="sxs-lookup"><span data-stu-id="71575-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="71575-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71575-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=Dirección IP:puerto\]**</span><span class="sxs-lookup"><span data-stu-id="71575-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-108">Especifica la dirección IP y el puerto para el enlace.</span><span class="sxs-lookup"><span data-stu-id="71575-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="71575-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span><span class="sxs-lookup"><span data-stu-id="71575-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-110">Especifica el hash SHA del certificado.</span><span class="sxs-lookup"><span data-stu-id="71575-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="71575-111">Este hash tiene una longitud de 20 bytes y se especifica como una cadena hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="71575-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="71575-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span><span class="sxs-lookup"><span data-stu-id="71575-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-113">Especifica el GUID para identificar la aplicación propietaria.</span><span class="sxs-lookup"><span data-stu-id="71575-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="71575-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="71575-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-115">Especifica el nombre del almacén del certificado.</span><span class="sxs-lookup"><span data-stu-id="71575-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="71575-116">El valor predeterminado es MY.</span><span class="sxs-lookup"><span data-stu-id="71575-116">Defaults to MY.</span></span> <span data-ttu-id="71575-117">El certificado debe almacenarse en el contexto del equipo local.</span><span class="sxs-lookup"><span data-stu-id="71575-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="71575-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="71575-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-119">Activa o desactiva la comprobación de revocación de certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="71575-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="71575-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="71575-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-121">Activa o desactiva el uso de solo el certificado de cliente almacenado en caché para la comprobación de revocación.</span><span class="sxs-lookup"><span data-stu-id="71575-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="71575-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="71575-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-123">Activa o desactiva la comprobación de uso.</span><span class="sxs-lookup"><span data-stu-id="71575-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="71575-124">Está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="71575-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="71575-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="71575-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-126">Especifica el intervalo de tiempo para comprobar si hay una lista de revocación de certificados (CRL) actualizada.</span><span class="sxs-lookup"><span data-stu-id="71575-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="71575-127">Si este valor es 0, la nueva CRL solo se actualiza si expira la anterior (en segundos).</span><span class="sxs-lookup"><span data-stu-id="71575-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="71575-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="71575-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-129">Especifica el intervalo de tiempo de espera en los intentos de recuperar la lista de revocación de certificados para la dirección URL remota (en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="71575-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="71575-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span><span class="sxs-lookup"><span data-stu-id="71575-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-131">Enumera los emisores de certificados que pueden ser de confianza.</span><span class="sxs-lookup"><span data-stu-id="71575-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="71575-132">Esta lista puede ser un subconjunto de los emisores de certificados que son de confianza para el equipo.</span><span class="sxs-lookup"><span data-stu-id="71575-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="71575-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="71575-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-134">Especifica el nombre del almacén en LOCAL \_ MACHINE donde se almacena SslCtlIdentifier.</span><span class="sxs-lookup"><span data-stu-id="71575-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="71575-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="71575-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-136">Activa o desactiva los asignadores de DS.</span><span class="sxs-lookup"><span data-stu-id="71575-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="71575-137">De forma predeterminada, está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="71575-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="71575-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="71575-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="71575-139">Activa o desactiva la negociación del certificado.</span><span class="sxs-lookup"><span data-stu-id="71575-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="71575-140">De forma predeterminada, está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="71575-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="71575-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71575-141">Examples</span></span>

<span data-ttu-id="71575-142">**add sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="71575-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="71575-143">**certhash=0102030405060708090A0B0C0D0E0F101121314**</span><span class="sxs-lookup"><span data-stu-id="71575-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="71575-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="71575-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




