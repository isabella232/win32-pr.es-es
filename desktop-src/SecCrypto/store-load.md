---
description: Importa certificados de un archivo en el almacén.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Método Store.Load
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
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897795"
---
# <a name="storeload-method"></a>Método Store.Load

\[El **método Load** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Load** importa certificados de un archivo en el almacén.

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

*FileName* \[ En\]
</dt> <dd>

Cadena que contiene la ruta de acceso a un archivo .cer, .sst, .spc, .p7s o .pfx, o a cualquier archivo con firma Authenticode.

</dd> <dt>

*Contraseña* \[ en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña de texto no cifrado del archivo. Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña. Para obtener información sobre cómo proteger la contraseña, vea [Control de contraseñas.](../secbp/handling-passwords.md)

</dd> <dt>

*KeyStorageFlag* \[ en, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ KEY \_ STORAGE \_ FLAG**](capicom-key-storage-flag.md) que define las marcas de almacenamiento de claves. El valor predeterminado es CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ DEFAULT**</dt> </dl>                       | Almacenamiento de claves predeterminado.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**ALMACENAMIENTO DE CLAVES \_ CAPICOM \_ \_ EXPORTABLE**</dt> </dl>              | La clave se puede exportar.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ KEY STORAGE USUARIO \_ \_ \_ PROTEGIDO**</dt> </dl> | La clave está protegida por el usuario.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si se **llama al método Load** en un almacén de memoria, los contenedores de claves que se crean se eliminarán cuando se elimine el almacén de memoria. Por ejemplo, si un archivo .pfx se carga en un almacén de memoria y, posteriormente, se agrega a un almacén del sistema (como Mi almacén) desde el almacén de memoria, el certificado del almacén Mi no contendrá una clave. En este caso, el archivo .pfx debe cargarse directamente en Mi almacén.

Este método genera CAPICOM \_ E NOT ALLOWED cuando se crea un script desde una aplicación basada en \_ \_ web.

Si la contraseña no puede descifrar el [](../secgloss/c-gly.md) archivo de clave privada, se debe consultar el proveedor de servicios criptográficos (CSP) predeterminado. Si el CSP predeterminado es el proveedor criptográfico base de Microsoft y se produce un error en la operación de descifrado, la operación de descifrado se debe intentar de nuevo con el proveedor criptográfico seguro de Microsoft o el proveedor de servicios criptográficos mejorado de Microsoft, lo que esté disponible.

Si el certificado que se carga en el almacén es el mismo que el que ya existe, el método **Load** eliminará el certificado existente del almacén y, a continuación, agregará el nuevo certificado. El nuevo certificado heredará las propiedades del certificado existente. El contenedor de claves privadas existente se reemplaza por el nuevo contenedor de claves privadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tienda**](store.md)
</dt> </dl>

 

 
