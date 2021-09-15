---
description: Proporciona acceso de solo lectura a las propiedades de uso clave de un certificado.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objeto KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473459"
---
# <a name="keyusage-object"></a>Objeto KeyUsage

\[El **objeto KeyUsage** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto KeyUsage** proporciona acceso de solo lectura a las propiedades de uso de claves de un certificado.

## <a name="members"></a>Members

El **objeto KeyUsage** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto KeyUsage** tiene estas propiedades.



| Propiedad.                                                                           | Tipo de acceso          | Descripción                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Solo lectura<br/> | Recupera un valor booleano que indica si la **extensión KeyUsage** está marcada como crítica.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Solo lectura<br/> | Recupera un valor booleano que indica si el bit CRLSign está establecido.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit dataEncipherment.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit decipherOnly.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit digitalSignature.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit encipherOnly.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit keyAgreement.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Solo lectura<br/> | Recupera un valor booleano que indica si el bit keyCertSign está establecido.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit keyEncipherment.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Solo lectura<br/> | Recupera un valor booleano que indica si se establece el bit nonRepudiationEnabled.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Solo lectura<br/> | Recupera un valor booleano que indica si la **extensión KeyUsage** está presente.<br/> Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **KeyUsage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
