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
ms.openlocfilehash: 8da0ad9681f3dd87227a7fe0b5a5419ceac4c7ee354fb1548427c100561e816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770844"
---
# <a name="certificatepolicies-object"></a>Objeto CertificatePolicies

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para recuperar las directivas de certificado.\]

El **objeto CertificatePolicies** representa una colección de [**objetos PolicyInformation.**](policyinformation.md) Cada [**objeto PolicyInformation**](policyinformation.md) representa una única directiva de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto CertificatePolicies** se usa para realizar las tareas siguientes:

-   Recupere el número de directivas de certificado de la colección.
-   Recupera un objeto [**PolicyInformation**](policyinformation.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto CertificatePolicies** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto CertificatePolicies** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](certificatepolicies-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.<br/>                                                                                                                    |
| [**Elemento**](certificatepolicies-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**PolicyInformation**](policyinformation.md) que representa la directiva de certificado indexada de la colección. Esta es la propiedad predeterminada.<br/>                                                    |



 

## <a name="remarks"></a>Comentarios

No **se puede crear el objeto CertificatePolicies.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
