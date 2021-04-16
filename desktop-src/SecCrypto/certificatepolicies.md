---
description: Colección de objetos PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objeto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690392"
---
# <a name="certificatepolicies-object"></a>Objeto CertificatePolicies

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]

El objeto **CertificatePolicies** representa una colección de objetos [**PolicyInformation**](policyinformation.md) . Cada objeto [**PolicyInformation**](policyinformation.md) representa una única directiva de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **CertificatePolicies** se usa para realizar las siguientes tareas:

-   Recupere el número de directivas de certificado de la colección.
-   Recupera un objeto [**PolicyInformation**](policyinformation.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **CertificatePolicies** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **CertificatePolicies** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](certificatepolicies-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.<br/>                                                                                                                    |
| [**Elemento**](certificatepolicies-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva de certificado indizada de la colección. Esta es la propiedad predeterminada.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **CertificatePolicies** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
