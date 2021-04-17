---
description: Establece o recupera las marcas de comprobación de validez de un certificado.
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: Propiedad CertificateStatus. CheckFlag
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
ms.openlocfilehash: 00b0c648de17f6aca931ab3f3417d9ecb53ac558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670613"
---
# <a name="certificatestatuscheckflag-property"></a>Propiedad CertificateStatus. CheckFlag

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **CheckFlag** establece o recupera las marcas de comprobación de validez de un certificado.

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de la [**\_ \_ marca de comprobación de CAPICOM**](capicom-check-flag.md) que describe las comprobaciones de validez del certificado. El valor predeterminado es **CAPICOM \_ check \_ online \_ All**.

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1:** El valor predeterminado es [**CAPICOM \_ comprobar \_ \_ validez**](capicom-check-flag.md)de la firma, la validez de la [**hora de comprobación de CAPICOM \_ \_ \_**](capicom-check-flag.md), [**CAPICOM \_ comprobar \_ \_ raíz de confianza**](capicom-check-flag.md)y la [**\_ cadena de comprobación \_ completa \_ de CAPICOM**](capicom-check-flag.md).

**CAPICOM 2,0 y versiones anteriores:** El valor predeterminado es [**CAPICOM \_ comprobar \_ la \_ validez**](capicom-check-flag.md)de la firma, la [**validez del tiempo de comprobación de CAPICOM \_ \_ \_**](capicom-check-flag.md)y [**CAPICOM \_ comprobar la \_ \_ raíz de confianza**](capicom-check-flag.md).

En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**CAPICOM \_ comprobar \_ \_ Restricciones básicas**</dt> </dl>                          | Comprueba las restricciones básicas. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**\_ \_ cadena completa de comprobación de CAPICOM \_**</dt> </dl>                                   | Comprueba la cadena completa. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**CAPICOM \_ comprobar \_ restricciones de nombres \_**</dt> </dl>                             | Comprueba las restricciones de nombre. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**CAPICOM \_ comprobar el \_ período de \_ validez anidado \_**</dt> </dl>          | Comprueba la validez anidada. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ comprobar \_ ninguno**</dt> </dl>                                                                  | No se realiza ninguna comprobación de la validez.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**CAPICOM \_ comprobar \_ todo sin conexión \_**</dt> </dl>                                            | Comprueba sin conexión todo. Las comprobaciones de revocación se realizan en todos los certificados de la cadena excepto en el certificado raíz. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**CAPICOM \_ comprobar \_ todo en línea \_**</dt> </dl>                                               | Comprueba todo en línea. Las comprobaciones de revocación se realizan en todos los certificados de la cadena excepto en el certificado raíz. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM \_ comprobar \_ el \_ Estado de revocación sin conexión \_**</dt> </dl> | Comprueba el estado de revocación de todos los certificados de la cadena usando solo las CRL sin conexión.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ comprobar \_ el \_ Estado de revocación en línea \_**</dt> </dl>    | Comprueba el estado de revocación de todos los certificados de la cadena mediante listas CRL disponibles en línea. Las CRL se descargan mediante la extensión CDP en el certificado.<br/> Si la CRL se ha descargado y no ha expirado, CAPICOM lo usa y no se conecta.<br/> Si una CRL no se ha descargado o no está actualizada, CAPICOM se conecta para intentar descargar la CRL.<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**comprobación de la validez de la firma de CAPICOM \_ \_ \_**</dt> </dl>                       | Comprueba las firmas válidas en todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**\_validez de \_ tiempo de comprobación de CAPICOM \_**</dt> </dl>                                      | Comprueba la validez de tiempo de todos los certificados de la cadena.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ comprobar \_ raíz de confianza \_**</dt> </dl>                                         | Comprueba si existe una raíz de confianza de la cadena de certificados.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
