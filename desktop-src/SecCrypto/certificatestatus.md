---
description: Contiene información sobre cómo construir una cadena de confianza de certificados.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objeto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770013"
---
# <a name="certificatestatus-object"></a>Objeto CertificateStatus

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto CertificateStatus** contiene información sobre cómo construir una cadena de confianza de certificado.

## <a name="members"></a>Miembros

El **objeto CertificateStatus** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto CertificateStatus** tiene estos métodos.



| Método                                                               | Descripción                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | Devuelve una [**colección de ID que**](oids.md) representa los ID de la directiva de aplicación.<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | Devuelve una [**colección de ID que**](oids.md) representa los 000 000 000 000 de directiva de certificado usados durante la creación de cadenas.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Devuelve el [**objeto EKU**](eku.md) usado para establecer los elementos EKU que se comprobarán al establecer el estado de validez de un certificado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto CertificateStatus** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](certificatestatus-certificates.md)<br/>               | Lectura/escritura<br/> | Establece o recupera la colección de certificados que se pueden usar para compilar la cadena de certificados.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No [**se admite la**](certificatestatus-certificates.md) propiedad Certificates.<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | Lectura/escritura<br/> | Marca de comprobación de validez. Los valores se pueden unir mediante un operador **OR** lógico. La marca de comprobación predeterminada [**es CAPICOM \_ CHECK ONLINE \_ \_ ALL**](capicom-check-flag.md).<br/>                                                                                     |
| [**Resultado**](certificatestatus-result.md)<br/>                           | Solo lectura<br/>  | Indica si el certificado es válido. La validez del certificado se comprueba mediante la configuración actual de la [**propiedad CheckFlag**](certificatestatus-checkflag.md) y la configuración de directiva del certificado. Esta es la propiedad predeterminada.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Lectura/escritura<br/> | Establece o recupera el período de tiempo antes de que se determine que una dirección URL es inaccesible.<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | Lectura/escritura<br/> | Establece o recupera la hora a la que se comprobó el certificado.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

No se puede crear el objeto **CertificateStatus.**

El método [**Certificate.IsValid**](certificate-isvalid.md) devuelve el objeto **CertificateStatus.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**Cadena**](chain.md)
</dt> </dl>

 

 
