---
description: Guarda los objetos de certificado en la colección.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificates. Save (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671695"
---
# <a name="certificatessave-method"></a>Certificates. Save (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Save** guarda los objetos de [**certificado**](certificate.md) en la colección.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del archivo de salida donde se guardarán los certificados.

</dd> <dt>

*Contraseña* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para un archivo de [*clave privada*](../secgloss/p-gly.md) . El valor predeterminado es la cadena vacía (""). Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña. Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> <dt>

*Guardar como* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de los [**\_ certificados CAPICOM \_ Save \_ as \_ Type**](capicom-certificates-save-as-type.md) que especifica el formato del archivo de salida. El valor predeterminado es CAPICOM \_ Certificates \_ Save \_ as \_ pfx. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                          | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**los \_ certificados \_ de CAPICOM se guardan \_ como \_ pfx**</dt> </dl>                      | Los certificados se guardan como un archivo PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**Los \_ certificados \_ de CAPICOM se guardan \_ como \_ pkcs7**</dt> </dl>                | Los certificados se guardan como PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**los \_ certificados \_ de CAPICOM se guardan \_ como \_ serializados**</dt> </dl> | Los certificados se guardan como serializados.<br/> |



 

</dd> <dt>

*ExportFlag* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la [**\_ \_ marca de exportación de CAPICOM**](capicom-export-flag.md) que especifica si se omiten los errores de exportación de claves privadas. El valor predeterminado es CAPICOM \_ Export \_ default. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**\_ \_ configuración predeterminada de CAPICOM**</dt> </dl>                                                                                                      | No se omiten los errores de exportación de clave privada.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**ERROR de exportación de CAPICOM \_ \_ omitir \_ \_ clave privada \_ no \_ exportable \_**</dt> </dl> | Se omiten los errores de exportación de clave privada.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

Los objetos de [**certificado**](certificate.md) se pueden recuperar mediante el método [**Store. Load**](store-load.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
