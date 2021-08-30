---
description: Guarda el certificado en un archivo.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: ICertificate2::Save (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ab734b4e80c7809b03b00a39d8960a5a42c928c67af3260d363ba2c9e9dab5ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126895"
---
# <a name="icertificate2save-method"></a>ICertificate2::Save (Método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Save** guarda el certificado en un archivo. Este método se introdujo en CAPICOM 2.0.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del archivo de salida donde se guardará el certificado.

</dd> <dt>

*Contraseña* \[ in, opcional\]
</dt> <dd>

Cadena que contiene la contraseña [*de texto no*](../secgloss/p-gly.md) cifrado para un archivo de [*clave*](../secgloss/p-gly.md) privada. La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación. Para obtener información sobre cómo proteger la contraseña, vea [Control de contraseñas.](../secbp/handling-passwords.md)

</dd> <dt>

*SaveAs* \[ in, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE**](capicom-certificate-save-as-type.md) que especifica el formato del archivo de salida. El valor predeterminado es **CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ CER**. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                  | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ CER**</dt> </dl> | El archivo de salida tendrá el formato de archivo .cer sin claves privadas guardadas.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**CERTIFICADO CAPICOM \_ \_ GUARDAR COMO \_ \_ PFX**</dt> </dl> | El archivo de salida tendrá el formato de archivo .pfx (PKCS 12) y también se guardarán las claves privadas asociadas que \# se puedan exportar.<br/> |



 

</dd> <dt>

*IncludeOption* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ CERTIFICATE \_ INCLUDE \_ OPTION**](capicom-certificate-include-option.md) que especifica cuántos certificados de la cadena se guardan en el archivo de salida. El valor predeterminado es CAPICOM \_ CERTIFICATE INCLUDE END ENTITY \_ \_ \_ \_ ONLY. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ INCLUDE \_ CHAIN \_ EXCEPT \_ ROOT**</dt> </dl> | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**EL CERTIFICADO CAPICOM \_ \_ INCLUYE CADENA \_ \_ COMPLETA**</dt> </dl>                    | Guarda la cadena de certificados completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CERTIFICADO CAPICOM \_ INCLUIR \_ SOLO ENTIDAD \_ \_ \_ FINAL**</dt> </dl>       | Guarda solo el certificado de entidad final<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método genera CAPICOM \_ E NOT ALLOWED cuando se crea un script desde una aplicación basada en \_ \_ web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
