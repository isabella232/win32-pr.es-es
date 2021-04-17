---
description: Carga un certificado de firma desde un archivo. pfx especificado.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Signer. Load (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671235"
---
# <a name="signerload-method"></a>Signer. Load (método)

\[El método **Load** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Load** carga un certificado de firma desde un archivo. pfx especificado.

## <a name="syntax"></a>Sintaxis


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nombre del archivo. pfx que contiene el certificado de firma.

</dd> <dt>

*Contraseña* \[ de opta\]
</dt> <dd>

Cadena que contiene la contraseña de texto no cifrado utilizada para abrir el archivo. Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña. El valor predeterminado es una cadena vacía (""). Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método carga el primer certificado en el archivo. pfx que tiene una clave privada asociada.

Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Firmante**](signer.md)
</dt> </dl>

 

 
