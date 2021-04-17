---
description: Importa un certificado de un archivo.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2:: Load (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670371"
---
# <a name="icertificate2load-method"></a>ICertificate2:: Load (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Load** importa un certificado de un archivo. Este método se presentó en CAPICOM 2,0.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Una cadena que contiene la ruta de acceso a un archivo. cer o. pfx que contiene los datos del certificado.

</dd> <dt>

*Contraseña* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene la contraseña de [*texto no cifrado*](../secgloss/p-gly.md) para el archivo de [*clave privada*](../secgloss/p-gly.md) . La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación. Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de marcas de almacenamiento de claves de CAPICOM que define las marcas de almacenamiento de claves. [**\_ \_ \_**](capicom-key-storage-flag.md) El valor predeterminado es CAPICOM \_ key \_ Storage \_ default. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ , \_ valor predeterminado de almacenamiento de claves \_**</dt> </dl>                       | Almacenamiento de claves predeterminado.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**el \_ almacenamiento de claves de CAPICOM \_ \_ exportable**</dt> </dl>              | La clave es exportable.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ \_ protección del \_ usuario de almacenamiento de claves \_**</dt> </dl> | La clave está protegida por el usuario.<br/> |



 

</dd> <dt>

*KeyLocation* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la [**\_ \_ Ubicación de la clave CAPICOM**](capicom-key-location.md) que define los tipos de ubicación de clave. El valor predeterminado es la \_ clave de usuario actual de CAPICOM \_ \_ . En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                               | Significado                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**\_tecla de \_ usuario \_ actual de CAPICOM**</dt> </dl>    | La clave es una clave de usuario.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**\_clave de \_ máquina \_ local de CAPICOM**</dt> </dl> | La clave es una clave del equipo.<br/> |



 

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



 

 
