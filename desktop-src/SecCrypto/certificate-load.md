---
description: Importa un certificado de un archivo.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: ICertificate2::Load (método)
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
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771553"
---
# <a name="icertificate2load-method"></a>ICertificate2::Load (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Load** importa un certificado de un archivo. Este método se introdujo en CAPICOM 2.0.

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

*FileName* \[ En\]
</dt> <dd>

Cadena que contiene la ruta de acceso a un archivo .cer o .pfx que contiene los datos del certificado.

</dd> <dt>

*Contraseña* \[ in, opcional\]
</dt> <dd>

Cadena que contiene la contraseña [*de texto no*](../secgloss/p-gly.md) cifrado del archivo de [*clave*](../secgloss/p-gly.md) privada. La contraseña puede contener hasta 32 caracteres Unicode, incluido un carácter nulo de terminación. Para obtener información sobre cómo proteger la contraseña, vea [Control de contraseñas.](../secbp/handling-passwords.md)

</dd> <dt>

*KeyStorageFlag* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ KEY \_ STORAGE \_ FLAG**](capicom-key-storage-flag.md) que define las marcas de almacenamiento de claves. El valor predeterminado es CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                           | Significado                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ DEFAULT**</dt> </dl>                       | Almacenamiento de claves predeterminado.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**ALMACENAMIENTO DE CLAVES \_ CAPICOM \_ \_ EXPORTABLE**</dt> </dl>              | La clave es exportable.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**CAPICOM \_ KEY \_ STORAGE \_ USER \_ PROTECTED**</dt> </dl> | La clave está protegida por el usuario.<br/> |



 

</dd> <dt>

*KeyLocation* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ KEY \_ LOCATION**](capicom-key-location.md) que define los tipos de ubicación clave. El valor predeterminado es CAPICOM \_ CURRENT \_ USER \_ KEY. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                               | Significado                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CLAVE DE USUARIO \_ ACTUAL DE CAPICOM \_ \_**</dt> </dl>    | La clave es una clave de usuario.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**CAPICOM \_ LOCAL \_ MACHINE \_ KEY**</dt> </dl> | La clave es una clave de máquina.<br/> |



 

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



 

 
