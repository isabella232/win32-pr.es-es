---
description: PNRP usa la función WSASetService para registrar o quitar nombres de mismo nivel.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP y WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667389"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP y WSASetService

PNRP usa la función [**WSASetService**](winsock-nsp-reference-links.md) para registrar o quitar [nombres de mismo nivel](peer-names.md).

## <a name="registering-a-name"></a>Registrar un nombre

El registro incluye un nombre del mismo nivel y un conjunto de puntos de conexión en los que se puede establecer contacto con un servicio. Un registro es específico de una nube PNRP. Una vez registrado un elemento del mismo nivel, se produce un retraso entre el registro y la propagación de la información de registro a otros nodos. Durante este tiempo, es posible que otros nodos no puedan resolver un elemento del mismo nivel registrado recientemente.

El registro del servicio no es persistente.

-   Si un proceso de cliente que registra un nombre del mismo nivel sale o llama a [**WSACleanup**](winsock-nsp-reference-links.md), se anula el registro del nombre del mismo nivel.
-   Si el proceso actual ya ha registrado un nombre de mismo nivel especificado en la misma nube, se reemplaza con nuevos valores de registro.

Al registrar un nombre del mismo nivel, se deben indicar los siguientes valores de parámetro:

-   el parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Register**.
-   el parámetro *dwControlFlags* debe ser cero (0).

Al registrar un nombre del mismo nivel, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRegInfo* debe contener los valores siguientes:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica un nombre del mismo nivel que se va a registrar. Si el [nombre del mismo nivel](peer-names.md) no es seguro, la identidad es opcional. Si la identidad se especifica como **null**, PNRP usa la identidad local de la máquina, de forma predeterminada.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser SVCID \_ PNRPNAME.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

ignorado. Sin embargo, sigue siendo necesario que la cadena tenga menos de 40 caracteres, incluido el terminador **null** .

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

Debe ser un nombre de nube, una cadena vacía o **null**. Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global". De lo contrario, debe apuntar a un nombre de nube válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Especifica el número de direcciones registradas por un servicio. El número máximo de direcciones que se pueden registrar para un único nombre es 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Puntero a una lista de direcciones que se van a registrar.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Se deben establecer los parámetros específicos de la estructura **PNRPINFO** . Para obtener más información, consulte la siguiente sección de la estructura **PNRPINFO** .

</dd> </dl>

## <a name="pnrpinfo-structure"></a>Estructura PNRPINFO

Si se establece el miembro **lpBlob** de la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) , se deben establecer los siguientes miembros de la estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Especifica la identidad del nombre del mismo nivel que se crea mediante [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Si un nombre del mismo nivel no es seguro, la identidad es opcional. Si la identidad se especifica como **null**, PNRP usa la identidad local del equipo, de forma predeterminada.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Especifica el número de segundos entre las operaciones de actualización.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Debe ser cero (0) o una **\_ sugerencia PNRPINFO**. El valor predeterminado es cero (0). Esto significa que la parte de la ubicación del servicio del identificador PNRP se genera mediante la dirección IP de **saHint**. De lo contrario, la ubicación del servicio se genera con la primera dirección IP en la primera entrada IPv6 del miembro **lpcsaBuffer** .

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica la dirección IPv6 de la sugerencia.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Anular el registro de un nombre de mismo nivel

La lista siguiente identifica la información importante sobre cómo anular el registro de un nombre de mismo nivel.

-   Solo una aplicación que registra un nombre del mismo nivel puede anular su registro.
-   Un nombre del mismo nivel no se registra automáticamente si se llama a [**WSACleanup**](winsock-nsp-reference-links.md) .
-   PNRP siempre quita el registro del nombre de servicio completo. No permite la eliminación de direcciones individuales.
-   Al anular el registro de un nombre, el parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Delete**.
-   PNRP no admite el valor **RNRSERVICE \_ unregister**.
-   El parámetro *dwControlFlags* debe ser cero (0).

Al anular el registro de un nombre, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRegInfo* debe contener los valores siguientes:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica el tamaño de esta estructura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica un nombre del mismo nivel del que se va a anular el registro.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Debe ser **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

ignorado. Se establece en **null**.

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

Debe ser un nombre de nube, una cadena vacía o **null**. Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global". De lo contrario, debe apuntar a un nombre de nube válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

ignorado. Se establece en **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

ignorado. Se establece en cero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . El miembro **lpszIdentity** de la estructura **lpBlob** identifica el nombre de la identidad que se usa para registrar un nombre del mismo nivel. Los miembros restantes se deben establecer en los mismos valores que se usan al registrar un nombre.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de error NSP de PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSASetService**
</dt> </dl>

 

 



