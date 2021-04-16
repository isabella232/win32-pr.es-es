---
description: Guarda el certificado en un archivo.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2:: Save (método)'
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
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690275"
---
# <a name="icertificate2save-method"></a>ICertificate2:: Save (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Save** guarda el certificado en un archivo. Este método se presentó en CAPICOM 2,0.

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

*Nombre de archivo* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del archivo de salida en el que se guardará el certificado.

</dd> <dt>

*Contraseña* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para un archivo de [*clave privada*](../secgloss/p-gly.md) . La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación. Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> <dt>

*Guardar como* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ \_ \_ tipo guardar como del certificado de CAPICOM**](capicom-certificate-save-as-type.md) que especifica el formato del archivo de salida. El valor predeterminado es **CAPICOM \_ Certificate \_ Save \_ as \_ cer**. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                  | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**\_certificado \_ de CAPICOM guardar \_ como \_ cer**</dt> </dl> | El archivo de salida se formateará como un archivo. cer sin ninguna clave privada guardada.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**el \_ certificado \_ de CAPICOM se guarda \_ como \_ pfx**</dt> </dl> | El archivo de salida se formateará como un archivo. pfx (PKCS \# 12) y las claves privadas asociadas que se puedan exportar también se guardarán.<br/> |



 

</dd> <dt>

*IncludeOption* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la [**\_ \_ \_ opción incluir certificado de CAPICOM**](capicom-certificate-include-option.md) que especifica cuántos certificados de la cadena se guardan en el archivo de salida. El valor predeterminado es el certificado de CAPICOM \_ \_ incluir \_ solo la \_ entidad final \_ . En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                             | Significado                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz**</dt> </dl> | Guarda todos los certificados de la cadena con la excepción de la entidad raíz.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**</dt> </dl>                    | Guarda la cadena de certificados completa<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**</dt> </dl>       | Guarda solo el certificado de entidad final<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
