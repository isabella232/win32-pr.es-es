---
description: Deriva una clave de sesión del secreto y cifra el valor de la propiedad de contenido usando esa clave. Devuelve el contenido cifrado como una cadena codificada.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: EncryptedData. Encrypt (método) (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670441"
---
# <a name="encrypteddataencrypt-method"></a>EncryptedData. Encrypt (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El método **Encrypt** deriva una clave de sesión del secreto y cifra el valor de la propiedad de [**contenido**](encrypteddata-content.md) usando esa clave. Devuelve el contenido cifrado como una cadena codificada.

## <a name="syntax"></a>Sintaxis


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación utilizado para codificar los datos cifrados. El valor predeterminado es CAPICOM \_ encode \_ Base64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ any**</dt> </dl>          | Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM, codificación \_ \_ Base64**</dt> </dl> | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_código binario de codificación de CAPICOM \_**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena que contiene los datos cifrados codificados.

## <a name="remarks"></a>Observaciones

Antes de llamar al método **Encrypt** , establezca la propiedad [**Content**](encrypteddata-content.md) y llame al método [**SetSecret**](encrypteddata-setsecret.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>                | <dl> <dt>InfoCard. h</dt> </dl>  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
