---
description: Genera una clave de sesión y cifra los datos y sobres.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Encrypt (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649709"
---
# <a name="envelopeddataencrypt-method"></a>EnvelopedData. Encrypt (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Encrypt** genera una clave de sesión, utiliza esa clave para cifrar el contenido, incluye el contenido cifrado de cada destinatario mediante el cifrado de la clave de sesión con la clave pública de cada destinatario y, a continuación, devuelve el [*BLOB*](../secgloss/b-gly.md) que contiene el contenido cifrado y las claves de sesión cifrada como una cadena codificada.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación utilizado para codificar los datos con doble cifrado. El valor de codificación predeterminado es CAPICOM \_ codificado en \_ Base64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ any**</dt> </dl>          | Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM, codificación \_ \_ Base64**</dt> </dl> | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_código binario de codificación de CAPICOM \_**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un BLOB que contiene los datos con doble cifrado en una cadena codificada.

## <a name="remarks"></a>Observaciones

El BLOB devuelto contiene el contenido cifrado y una clave de sesión cifrada para cada destinatario previsto. Estas claves de sesión se cifran mediante la clave pública de cada destinatario. Las claves de sesión cifradas solo se pueden descifrar con la clave privada de un destinatario.

Si la propiedad [**Recipients**](envelopeddata-recipients.md) no contiene ninguna información, este método busca en el almacén de certificados AddressBook del usuario actual los destinatarios potenciales. Si se encuentra más de un posible destinatario, se solicita al usuario que seleccione un destinatario en un cuadro de diálogo de selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
