---
description: Establece o recupera un valor de enumeración que especifica el nombre de CAPICOM del EKU. Esta es la propiedad predeterminada.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'IEKU:: Name (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649995"
---
# <a name="iekuname-property"></a>IEKU:: Name (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **Name** establece o recupera un valor de enumeración que especifica el nombre de CAPICOM del EKU. Esta es la propiedad predeterminada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de [**\_ EKU de CAPICOM**](capicom-eku.md) que especifica el nombre de CAPICOM del EKU. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**EKU de CAPICOM \_ \_ otro**</dt> </dl>                                                      | El certificado tiene usos definidos en la directiva local. Se usa si el EKU necesario no está predefinido y la aplicación debe establecer el valor de OID.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**\_autenticación del \_ servidor \_ EKU de CAPICOM**</dt> </dl>                                   | El certificado se puede usar para autenticar un servidor.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**\_autenticación de \_ cliente de EKU de CAPICOM \_**</dt> </dl>                                   | El certificado se puede utilizar para autenticar a un cliente.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**\_firma de \_ código \_ EKU de CAPICOM**</dt> </dl>                                | El certificado se puede utilizar para crear una firma digital.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**\_protección de \_ correo electrónico de EKU de CAPICOM \_**</dt> </dl>                    | El certificado se puede usar para la protección de correo electrónico.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**\_Inicio de \_ sesión con tarjeta inteligente EKU de CAPICOM \_**</dt> </dl>                       | El certificado se puede usar para el inicio de sesión con tarjeta inteligente. Introducido en CAPICOM 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**\_sistema de \_ cifrado de \_ archivos \_ EKU de CAPICOM**</dt> </dl> | El certificado se puede usar para EFS. Introducido en CAPICOM 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Observaciones

Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
