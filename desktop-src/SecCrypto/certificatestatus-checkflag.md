---
description: Establece o recupera las marcas de comprobación de validez de un certificado.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: Propiedad CertificateStatus.CheckFlag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877455"
---
# <a name="certificatestatuscheckflag-property"></a>Propiedad CertificateStatus.CheckFlag

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad CheckFlag** establece o recupera las marcas de comprobación de validez de un certificado.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valor de propiedad

Valor de la enumeración [**CAPICOM \_ CHECK \_ FLAG**](capicom-check-flag.md) que describe las comprobaciones de validez del certificado. El valor predeterminado es **CAPICOM \_ CHECK \_ ONLINE \_ ALL**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** El valor predeterminado es [**CAPICOM \_ CHECK \_ SIGNATURE \_ VALIDITY**](capicom-check-flag.md), [**CAPICOM \_ CHECK TIME \_ \_ VALIDITY**](capicom-check-flag.md), [**CAPICOM \_ CHECK TRUSTED \_ \_ ROOT**](capicom-check-flag.md)y [**CAPICOM \_ CHECK COMPLETE \_ \_ CHAIN**](capicom-check-flag.md).

**CAPICOM 2.0 y versiones anteriores:** El valor predeterminado es [**CAPICOM \_ CHECK \_ SIGNATURE \_ VALIDITY**](capicom-check-flag.md), [**CAPICOM \_ CHECK TIME \_ \_ VALIDITY**](capicom-check-flag.md)y [**CAPICOM \_ CHECK TRUSTED \_ \_ ROOT**](capicom-check-flag.md).

En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**RESTRICCIONES \_ \_ BÁSICAS DE CAPICOM CHECK \_**</dt> </dl>                          | Comprueba las restricciones básicas. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**CAPICOM \_ CHECK \_ COMPLETE \_ CHAIN**</dt> </dl>                                   | Comprueba la cadena completa. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**RESTRICCIONES \_ DE CAPICOM CHECK \_ \_ NAME**</dt> </dl>                             | Comprueba las restricciones de nombre. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**CAPICOM \_ CHECK \_ NESTED \_ VALIDITY \_ PERIOD**</dt> </dl>          | Comprueba la validez anidada. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ CHECK \_ NONE**</dt> </dl>                                                                  | No se realiza ninguna comprobación de validez.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ OFFLINE \_ ALL**</dt> </dl>                                            | Comprueba todo sin conexión. Las comprobaciones de revocación se realizan en todos los certificados de la cadena, excepto en el certificado raíz. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ CHECK \_ ONLINE \_ ALL**</dt> </dl>                                               | Comprueba todo en línea. Las comprobaciones de revocación se realizan en todos los certificados de la cadena, excepto en el certificado raíz. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS**</dt> </dl> | Comprueba el estado de revocación de todos los certificados de la cadena solo mediante CRL sin conexión.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS**</dt> </dl>    | Comprueba el estado de revocación de todos los certificados de la cadena mediante CRL disponibles en línea. Las CRL se descargan mediante la extensión CDP en el certificado.<br/> Si la CRL se ha descargado y no ha expirado, CAPICOM la usa y no está en línea.<br/> Si no se ha descargado una CRL o no está actualizada, CAPICOM se queda en línea para intentar descargar la CRL.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**VALIDEZ DE LA \_ FIRMA CAPICOM CHECK \_ \_**</dt> </dl>                       | Comprueba si hay firmas válidas en todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**VALIDEZ DE LA \_ HORA \_ DE COMPROBACIÓN DE CAPICOM \_**</dt> </dl>                                      | Comprueba la validez de la hora de todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**</dt> </dl>                                         | Comprueba si hay una raíz de confianza de la cadena de certificados.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
