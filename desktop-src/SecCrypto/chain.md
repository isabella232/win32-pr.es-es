---
description: Representa una cadena de confianza de certificado.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690246"
---
# <a name="chain-object"></a>Chain (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto de **cadena** representa una cadena de confianza de certificado.

Este objeto proporciona propiedades y métodos para crear una cadena de confianza de certificados para comprobar la validez de los certificados. La cadena se genera mediante el valor de la propiedad [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) y la configuración de directiva de un objeto [**CertificateStatus**](certificatestatus.md) .

El objeto **Chain** expone las siguientes interfaces:

-   **IChain2**: introducido en CAPICOM 2,0.
-   **IChain**: introducido en CAPICOM 1,0.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **cadena** se usa para realizar las siguientes tareas:

-   Cree una cadena de confianza de certificados.
-   Obtenga los OID de todas las directivas de aplicación y certificado válidas para la cadena.
-   Compruebe el estado de los certificados de la cadena.
-   Obtener información de error extendida.
-   Recupere la colección de certificados de la cadena.

## <a name="members"></a>Miembros

El objeto de **cadena** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **cadena** tiene estos métodos.



| Método                                                   | Descripción                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de aplicación válidos para la cadena.<br/> (Se hereda de **ChainIChain2**)                                                                                                                                                          |
| [**Build**](chain-build.md)                             | Crea una cadena de comprobación de certificados desde un certificado final al [*certificado raíz*](../secgloss/r-gly.md)de confianza, y devuelve un valor booleano que indica la validez global de la cadena.<br/> (Se hereda de **ChainIChain2IChain**) |
| [**CertificatePolicies**](chain-certificatepolicies.md) | Devuelve una colección de [**OID**](oids.md) que representa los OID de directiva de certificado válidos para la cadena.<br/> (Se hereda de **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Devuelve una cadena que contiene información de error adicional sobre la entrada indizada.<br/> (Se hereda de **ChainIChain2**)                                                                                                                                                                                 |



 

### <a name="properties"></a>Propiedades

El objeto de **cadena** tiene estas propiedades.



| Propiedad                                              | Tipo de acceso          | Descripción                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](chain-certificates.md)<br/> | Solo lectura<br/> | Recupera una colección de [**certificados**](certificates.md) que representa los certificados de la cadena. Esta es la propiedad predeterminada.<br/> (Se hereda de **ChainIChain2IChain**) |
| [**Status**](chain-status.md)<br/>             | Solo lectura<br/> | Recupera el estado de validez de la cadena o de un certificado específico de la cadena.<br/> (Se hereda de **ChainIChain2IChain**)                                                       |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **cadena** y es seguro para el scripting. El ProgID del objeto de **cadena** es "CAPICOM. Chain. 2 ".

**CAPICOM 1. *x*:** el ProgID del objeto de **cadena** es CAPICOM. Cadena. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
