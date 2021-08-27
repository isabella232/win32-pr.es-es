---
description: Guarda los objetos Certificate en la colección.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Método Certificates.Save
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
ms.openlocfilehash: c3d724a6859a1fbc7765822227290facfb2c2f021fce2f5815f32c5e91fe6453
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126765"
---
# <a name="certificatessave-method"></a>Método Certificates.Save

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Save** guarda los objetos [**Certificate**](certificate.md) en la colección.

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

*FileName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del archivo de salida donde se guardarán los certificados.

</dd> <dt>

*Contraseña* \[ en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña [*de texto no*](../secgloss/p-gly.md) cifrado para un archivo de [*clave*](../secgloss/p-gly.md) privada. El valor predeterminado es la cadena vacía (""). Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña. Para obtener información sobre cómo proteger la contraseña, vea [Control de contraseñas.](../secbp/handling-passwords.md)

</dd> <dt>

*SaveAs* \[ en, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ CERTIFICATES \_ SAVE AS \_ \_ TYPE**](capicom-certificates-save-as-type.md) que especifica el formato del archivo de salida. El valor predeterminado es CAPICOM \_ CERTIFICATES \_ SAVE AS \_ \_ PFX. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                          | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**CERTIFICADOS CAPICOM \_ \_ GUARDADOS \_ COMO \_ PFX**</dt> </dl>                      | Los certificados se guardan como PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**LOS CERTIFICADOS CAPICOM \_ \_ SE \_ GUARDARÁN COMO \_ PKCS7**</dt> </dl>                | Los certificados se guardan como PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**LOS CERTIFICADOS CAPICOM \_ \_ SE \_ GUARDARÁN COMO \_ SERIALIZADOS**</dt> </dl> | Los certificados se guardan como serializados.<br/> |



 

</dd> <dt>

*ExportFlag* \[ en, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ EXPORT \_ FLAG**](capicom-export-flag.md) que especifica si se omiten los errores de exportación de claves privadas. El valor predeterminado es CAPICOM \_ EXPORT \_ DEFAULT. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**CAPICOM \_ EXPORT \_ DEFAULT**</dt> </dl>                                                                                                      | No se omiten los errores de exportación de clave privada.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**ERROR NO \_ EXPORTABLE DE \_ LA CLAVE PRIVADA OMITIBLE \_ DE LA \_ \_ \_ EXPORTACIÓN DE \_ CAPICOM**</dt> </dl> | Se omiten los errores de exportación de clave privada.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método genera CAPICOM \_ E NOT ALLOWED cuando se crea un script desde una aplicación basada en \_ \_ web.

Los [**objetos Certificate**](certificate.md) se pueden recuperar mediante el método [**Store.Load.**](store-load.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
