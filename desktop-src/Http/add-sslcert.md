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
# <a name="add-sslcert"></a>add sslcert

Agrega un nuevo enlace Capa de sockets seguros de certificado de servidor (SSL) y las directivas de certificado de cliente correspondientes para una dirección IP y un puerto.

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

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=Dirección IP:puerto\]**
</dt> <dd>

Especifica la dirección IP y el puerto para el enlace.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**
</dt> <dd>

Especifica el hash SHA del certificado. Este hash tiene una longitud de 20 bytes y se especifica como una cadena hexadecimal.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**
</dt> <dd>

Especifica el GUID para identificar la aplicación propietaria.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**
</dt> <dd>

Especifica el nombre del almacén del certificado. El valor predeterminado es MY. El certificado debe almacenarse en el contexto del equipo local.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**
</dt> <dd>

Activa o desactiva la comprobación de revocación de certificados de cliente.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**
</dt> <dd>

Activa o desactiva el uso de solo el certificado de cliente almacenado en caché para la comprobación de revocación.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**
</dt> <dd>

Activa o desactiva la comprobación de uso. Está habilitada de forma predeterminada.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**
</dt> <dd>

Especifica el intervalo de tiempo para comprobar si hay una lista de revocación de certificados (CRL) actualizada. Si este valor es 0, la nueva CRL solo se actualiza si expira la anterior (en segundos).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**
</dt> <dd>

Especifica el intervalo de tiempo de espera en los intentos de recuperar la lista de revocación de certificados para la dirección URL remota (en milisegundos).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**
</dt> <dd>

Enumera los emisores de certificados que pueden ser de confianza. Esta lista puede ser un subconjunto de los emisores de certificados que son de confianza para el equipo.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**
</dt> <dd>

Especifica el nombre del almacén en LOCAL \_ MACHINE donde se almacena SslCtlIdentifier.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**
</dt> <dd>

Activa o desactiva los asignadores de DS. De forma predeterminada, está deshabilitada.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**
</dt> <dd>

Activa o desactiva la negociación del certificado. De forma predeterminada, está deshabilitada.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**add sslcert ipport=1.1.1.1:443**

**certhash=0102030405060708090A0B0C0D0E0F101121314**

**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




