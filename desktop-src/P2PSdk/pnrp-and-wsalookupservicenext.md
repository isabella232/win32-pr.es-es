---
description: PNRP usa la función WSALookupServiceNext para hacer coincidir las consultas especificadas en una llamada anterior a WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP y WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667396"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP y WSALookupServiceNext

PNRP usa la función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para hacer coincidir las consultas especificadas en una llamada anterior a **WSALookupServiceBegin**. Los resultados de la función **WSALookupServiceNext** se determinan mediante la configuración de la estructura **WSAQUERYSET** pasada en la llamada de función **WSALookupServiceBegin** inicial. Esta función se usa para realizar las dos funciones siguientes:

-   Resolver un nombre de mismo nivel en una lista de direcciones
-   Enumerar nubes de red

Mediante el uso de [**WSANSPIoctl**](winsock-nsp-reference-links.md), el servicio de búsqueda se puede usar de forma asincrónica. Para obtener información sobre el uso de las funciones del servicio de búsqueda de forma asincrónica, vea [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md).

La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloquea incluso si se llama a **WSANSPIoctl** . Antes de llamar a **WSALookupServiceNext**, una aplicación debe esperar hasta que reciba una notificación, si el bloqueo es un problema.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Resolver un nombre de mismo nivel en una lista de direcciones

Al resolver un nombre de mismo nivel en una lista de direcciones, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) devuelta en el parámetro *lpqsResults* contiene los siguientes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Devuelve el tamaño de la estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Devuelve un nombre del mismo nivel: si se especifica **LUP \_ \_**, **LUP \_ devolverá \_ All** o **null** .

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Devuelve **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Devuelve un Comentario: si se especifica **LUP \_ Return \_ comment**, **LUP \_ Return \_ All** o **null** .

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Devuelve **\_ PNRPNAME NS**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Devuelve **el \_ proveedor NS \_ PNRPNAME**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Devuelve el nombre de la nube si se especifica **LUP \_ Return \_ Name**, **LUP \_ Return \_ All** o **null** .

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Devuelve cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Devuelve el número de entradas de la matriz de información de CSADDR \_ si **LUP \_ devuelve \_ addr**, **LUP \_ devuelve \_ All** o se especifica **null** . Este valor y la información de **lpcsaBuffer** son los bits clave de la información que se devuelve en esta estructura.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Devuelve un puntero a una matriz de \_ estructuras de información CSADDR si **LUP \_ devuelve \_ addr**, **LUP \_ devuelve \_ All** o se especifica **null** . Este búfer y el valor de **dwNumberOfCsAddrs** son los bits de información clave devueltos en esta estructura.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Devuelve cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Devuelve **null**.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Enumerar nubes de red

Al enumerar las nubes, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) devuelta en el parámetro *lpqsResults* contiene los siguientes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Devuelve el tamaño de la estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Devuelve un nombre de nube: si se especifica **\_ \_ el nombre de retorno LUP**, **LUP \_ devuelve \_ All** o **null** .

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Devuelve **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Devuelve **\_ PNRPCLOUD NS**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Devuelve **el \_ proveedor NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Devuelve cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Devuelve cero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Devuelve **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Devuelve cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Devuelve un puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) : Si **LUP \_ devuelve \_ BLOB**, **LUP \_ devuelve \_ All** o se especifica **null** .

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Estructura PNRPCLOUDINFO

Al enumerar los nombres de nube, se devuelven los siguientes valores en la estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Administración**
</dt> <dd>

Valor real de la nube.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Estado actual de una nube. [**PNRP \_ \_Estado de nube**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) especifica los valores válidos.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indica que un nombre de nube es válido en una red o solo es válido en un equipo actual. [**PNRP \_ \_Marcas de nube**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) especifica los valores válidos. Algunos nombres de nube son válidos en cualquier equipo de la misma red. Otros nombres de nube solo son válidos en un equipo actual y solo pueden ser válidos durante un período de tiempo.

-   Si **enCloudFlags** se establece en **PNRP \_ Cloud \_ name \_ local,** el nombre solo es válido de forma local.
-   Si no se establece **enCloudFlags** , el nombre de la nube se puede transferir a otros equipos.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de error NSP de PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



