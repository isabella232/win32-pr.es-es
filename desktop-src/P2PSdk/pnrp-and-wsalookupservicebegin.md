---
description: PNRP usa la función WSALookupServiceBegin para iniciar el proceso que permite a una aplicación hacer lo siguiente.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP y WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553405"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP y WSALookupServiceBegin

PNRP usa la [**función WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar el proceso que permite a una aplicación hacer lo siguiente:

-   [Resolución de un nombre](#resolving-a-name)
-   [Enumeración de nubes de red](#enumerating-network-clouds)

Los clientes que intentan realizar una de las funciones usan las funciones [**WSALookupServiceBegin,**](winsock-nsp-reference-links.md) **WSALookupServiceNext** y **WSALookupServiceEnd.**

Mediante el [**uso de WSANSPIoctl,**](winsock-nsp-reference-links.md)el servicio de búsqueda se puede usar de forma asincrónica. Para obtener información sobre el uso de las funciones de servicio de búsqueda de forma asincrónica, vea [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md).

El proceso para trabajar con nombres del mismo nivel es diferente del trabajo con nubes. Cada proceso se describe por separado en este tema.

## <a name="resolving-a-name"></a>Resolver un nombre

Una aplicación usa [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obtener la dirección IP, el puerto y el protocolo de un servicio del mismo nivel que está registrado en otro equipo. La **función WSALookupServiceBegin** se usa para iniciar el proceso de resolución de nombres y configurar los parámetros y las restricciones. Se devuelve un identificador y se debe usar al llamar a **WSALookupServiceNext** y **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Al resolver un nombre del mismo nivel, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los valores siguientes:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica un nombre del mismo nivel que se resolverá.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser **SVCID \_ PNRPNAME.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Debe ser **NS \_ PNRPNAME o** **NS \_ ALL.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Debe ser **NS \_ PROVIDER \_ PNRPNAME** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Debe ser un nombre de nube, una cadena vacía o **NULL.** Si este valor es **NULL o** una cadena vacía, se usa la nube predeterminada, \_ "Global". De lo contrario, debe apuntar a un nombre de nube válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Debe ser un puntero a una estructura [**BLOB**](winsock-nsp-reference-links.md) o **NULL.** Si es **NULL, se** usan los valores predeterminados. Si se establece, **lpBlob** apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) y se deben establecer parámetros específicos en la estructura **PNRPINFO.** Para obtener más información, vea las descripciones siguientes de la estructura PNRPINFO.

</dd> </dl>

PNRPINFO (estructura)

Si se establece el miembro **lpBlob** de la estructura [**LPWSAQUERYSET,**](pnrp-and-wsaqueryset.md) se deben establecer los siguientes miembros de la estructura [**PNRPINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Especifica el número solicitado de resoluciones.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Especifica el período de tiempo de espera solicitado para esperar respuestas. El valor predeterminado es 30 segundos. El máximo es 600 segundos (10 minutos).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Debe ser uno de los valores permitidos. El valor predeterminado es **PNRP \_ RESOLVE CRITERIA NON CURRENT PROCESS PEER \_ \_ \_ \_ \_ \_ NAME**. PNRP RESOLVE CRITERIA especifica valores [**\_ \_ válidos.**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Debe ser cero (0) o **PNRPINFO \_ HINT**. El valor predeterminado es cero (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica la dirección IP de la sugerencia. La sugerencia se usa al intentar encontrar el nombre del mismo nivel más cercano. El formato de la sugerencia es una dirección IPv6. Si **no se especifica saHint** al buscar el nombre del mismo nivel más cercano, en su lugar se usa una dirección IPv6 del equipo local. Este miembro se omite si **dwFlags** no está establecido.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

PNRP admite las siguientes marcas \_ LUP \_ \* RETURN:



| Valor                | Descripción                                |
|----------------------|--------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_    | Devuelve un nombre y un contexto.                |
| COMENTARIO DE \_ DEVOLUCIÓN DE LUP \_ | Devuelve un comentario asociado a un nombre.  |
| LUP \_ RETURN \_ ADDR    | Devuelve una dirección asociada a un nombre. |



 

## <a name="enumerating-network-clouds"></a>Enumeración de nubes de red

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Al enumerar nubes, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los valores siguientes:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Debe ser **NULL.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser **SVCID \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Debe ser **NS \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Debe ser **NS \_ PROVIDER \_ PNRPCLOUD** o **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reservado, debe ser **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntero a una [**estructura BLOB**](winsock-nsp-reference-links.md) que apunta a una [**estructura PNRPCLOUDINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) Si **lpBlob** es **NULL,** se enumeran todas las nubes.

</dd> </dl>

PNRPCLOUDINFO (estructura)

Al enumerar nubes, se deben establecer los siguientes miembros de [**la estructura PNRPCLOUDINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nube**
</dt> <dd>

Apunta a una estructura que especifica los criterios que puede usar para filtrar los resultados de la búsqueda. El **miembro Cloud.Scope puede** ser **PNRP SCOPE \_ \_ ANY**, **PNRP GLOBAL \_ \_ SCOPE**, **PNRP SITE LOCAL \_ \_ \_ SCOPE** o **PNRP LINK LOCAL \_ \_ \_ SCOPE**. Si **se especifica \_ PNRP SCOPE \_ ANY,** se devuelven todas las nubes. De lo contrario, solo se devuelven las nubes que coinciden **con Cloud.Scope.**

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Reservado, debe ser cero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

PNRP admite las siguientes marcas \_ LUP \_ \* RETURN:



| Valor             | Descripción                                                       |
|-------------------|-------------------------------------------------------------------|
| NOMBRE DEVUELTO DE LUP \_ \_ | Devuelve un nombre y un contexto.                                       |
| BLOB DE \_ DEVOLUCIÓN DE \_ LUP | Devuelve el [BLOB](pnrp-and-blob.md) asociado a esta nube. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP y WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de error de PNRP NSP](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



