---
description: Importa los certificados de un archivo en el almacén.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671837"
---
# <a name="storeload-method"></a>Store. Load (método)

\[El método **Load** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Load** importa los certificados de un archivo en el almacén.

## <a name="syntax"></a>Sintaxis


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

La cadena que contiene la ruta de acceso a un archivo. cer,. SST,. SPC,. p7s o. pfx, o cualquier archivo firmado con Authenticode.

</dd> <dt>

*Contraseña* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña de texto no cifrado del archivo. Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña. Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de marcas de almacenamiento de claves de CAPICOM que define las marcas de almacenamiento de claves. [**\_ \_ \_**](capicom-key-storage-flag.md) El valor predeterminado es CAPICOM \_ key \_ Storage \_ default. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ , \_ valor predeterminado de almacenamiento de claves \_**</dt> </dl>                       | Almacenamiento de claves predeterminado.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**el \_ almacenamiento de claves de CAPICOM \_ \_ exportable**</dt> </dl>              | La clave es exportable.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ \_ protección del \_ usuario de almacenamiento de claves \_**</dt> </dl> | La clave está protegida por el usuario.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se llama al método **Load** en un almacén de memoria, los contenedores de claves creados se eliminarán cuando se elimine el almacén de memoria. Por ejemplo, si se carga un archivo. pfx en un almacén de memoria y posteriormente se agrega a un almacén del sistema (por ejemplo, el almacén My) del almacén de memoria, el certificado del almacén My no contendrá una clave. En este caso, el archivo. pfx debe cargarse directamente en mi almacén.

Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

Si la contraseña no puede descifrar el archivo de clave privada, se debe consultar el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) predeterminado. Si el CSP predeterminado es el proveedor de servicios criptográficos de base de Microsoft y se produce un error en la operación de descifrado, se debe volver a intentar la operación de descifrado con el proveedor de servicios criptográficos seguros de Microsoft o con el proveedor de cifrado mejorado de Microsoft, lo que esté disponible

Si el certificado que se carga en el almacén es el mismo que el que ya existe, el método **Load** eliminará el certificado existente del almacén y, a continuación, agregará el nuevo certificado. El nuevo certificado heredará las propiedades del certificado existente. El contenedor de claves privadas existente se reemplaza por el nuevo contenedor de claves privadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
