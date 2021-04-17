---
description: PNRP usa la función WSALookupServiceBegin para iniciar el proceso que permite que una aplicación realice lo siguiente.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP y WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105670209"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP y WSALookupServiceBegin

PNRP usa la función [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar el proceso que permite a una aplicación realizar lo siguiente:

-   [Resolver un nombre](#resolving-a-name)
-   [Enumerar nubes de red](#enumerating-network-clouds)

Los clientes que intentan realizar una de las funciones usan las funciones [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** y **WSALookupServiceEnd** .

Mediante el uso de [**WSANSPIoctl**](winsock-nsp-reference-links.md), el servicio de búsqueda se puede usar de forma asincrónica. Para obtener información sobre el uso de las funciones del servicio de búsqueda de forma asincrónica, vea [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md).

El proceso para trabajar con nombres del mismo nivel es diferente de trabajar con nubes. Cada proceso se describe por separado en este tema.

## <a name="resolving-a-name"></a>Resolver un nombre

Una aplicación utiliza [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obtener la dirección IP, el puerto y el protocolo para un servicio del mismo nivel registrado en otro equipo. La función **WSALookupServiceBegin** se usa para iniciar el proceso de resolución de nombres y configurar los parámetros y las restricciones. Se devuelve un identificador y se debe usar al llamar a **WSALookupServiceNext** y **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Al resolver un nombre del mismo nivel, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los siguientes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica el nombre del mismo nivel que se va a resolver.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Debe ser **NS \_ PNRPNAME** o **NS \_ All**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Debe ser un **\_ proveedor NS \_ PNRPNAME** o **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Debe ser un nombre de nube, una cadena vacía o **null**. Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global \_ ". De lo contrario, debe apuntar a un nombre de nube válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Debe ser un puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) o **null**. Si es **null**, se usan los valores predeterminados. Si se establece, **lpBlob** apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) y se deben establecer los parámetros específicos de la estructura **PNRPINFO** . Para obtener más información, vea las siguientes descripciones de la estructura PNRPINFO.

</dd> </dl>

Estructura PNRPINFO

Si se establece el miembro **lpBlob** de la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) , se deben establecer los siguientes miembros de la estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Especifica el número solicitado de resoluciones.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Especifica el período de tiempo de espera solicitado para la espera de respuestas. El valor predeterminado es 30 segundos. El máximo es de 600 segundos (10 minutos).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Debe ser uno de los valores permitidos. El valor predeterminado es **PNRP \_ resolver \_ criterios \_ no \_ actual \_ \_ \_ nombre del mismo nivel**. Los valores válidos se especifican mediante los [**\_ \_ criterios de resolución de PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Debe ser cero (0) o una **\_ sugerencia PNRPINFO**. El valor predeterminado es cero (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica la dirección IP de la sugerencia. La sugerencia se usa al intentar buscar el nombre del mismo nivel más cercano. El formato de la sugerencia es una dirección IPv6. Si no se especifica **saHint** al buscar el nombre del mismo nivel más cercano, se usa en su lugar una dirección IPv6 del equipo local. Este miembro se omite si **dwFlags** no está establecido.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

\_PNRP admite las siguientes marcas devueltas de LUP \_ \* :



| Value                | Descripción                                |
|----------------------|--------------------------------------------|
| \_nombre devuelto de LUP \_    | Devuelve un nombre y un contexto.                |
| LUP \_ Comentario devuelto \_ | Devuelve un comentario asociado a un nombre.  |
| LUP \_ devolver \_ dirección    | Devuelve una dirección asociada a un nombre. |



 

## <a name="enumerating-network-clouds"></a>Enumerar nubes de red

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Al enumerar las nubes, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los valores siguientes:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Debe ser **null**.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Debe ser **NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Debe ser un **\_ proveedor NS \_ PNRPCLOUD** o **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserved, debe ser **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) . Si **lpBlob** es **null**, se enumeran todas las nubes.

</dd> </dl>

Estructura PNRPCLOUDINFO

Al enumerar nubes, se deben establecer los siguientes miembros de la estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Administración**
</dt> <dd>

Apunta a una estructura que especifica los criterios que se pueden usar para filtrar los resultados de la búsqueda. El **miembro Cloud. Scope** puede ser **el \_ ámbito \_ PNRP any**, el **\_ \_ ámbito global PNRP**, el **\_ \_ \_ ámbito local del sitio PNRP** o el **\_ \_ \_ ámbito local del vínculo PNRP**. Si se especifica el **\_ ámbito PNRP \_ any** , se devuelven todas las nubes. De lo contrario, solo se devuelven las nubes que coinciden con la **nube. el ámbito** .

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Reserved, debe ser cero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

\_PNRP admite las siguientes marcas devueltas de LUP \_ \* :



| Value             | Descripción                                                       |
|-------------------|-------------------------------------------------------------------|
| \_nombre devuelto de LUP \_ | Devuelve un nombre y un contexto.                                       |
| LUP \_ devolver \_ BLOB | Devuelve el [BLOB](pnrp-and-blob.md) asociado a esta nube. |



 

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

[Códigos de error NSP de PNRP](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



