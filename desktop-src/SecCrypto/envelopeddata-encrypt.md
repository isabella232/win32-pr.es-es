---
description: Genera una clave de sesión y cifra y sobres los datos.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Método EnvelopedData.Encrypt
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
ms.openlocfilehash: df4741538ae11dbe1b158fd9b8e8a6c8632c427f9a0e8376e8cd10c9056461fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766095"
---
# <a name="envelopeddataencrypt-method"></a>Método EnvelopedData.Encrypt

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Encrypt** genera una clave de sesión, usa esa clave para cifrar el contenido, envuelve el contenido cifrado para cada destinatario mediante el cifrado de la clave de sesión con la clave pública de cada destinatario y, a continuación, devuelve el [*BLOB*](../secgloss/b-gly.md) que contiene el contenido cifrado y las claves de sesión cifradas como una cadena codificada.

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

Valor de la enumeración [**\_ CAPICOM ENCODING \_ TYPE**](capicom-encoding-type.md) que indica el tipo de codificación utilizado para codificar los datos sobreados. El valor de codificación predeterminado es CAPICOM \_ ENCODE \_ BASE64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Este tipo de codificación solo se usa cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, se usará CAPICOM \_ ENCODE \_ BASE64 en su lugar. Introducido en CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CODIFICACIÓN \_ CAPICOM \_ BASE64**</dt> </dl> | Los datos se guardan como una cadena codificada en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un BLOB que contiene los datos sobreados en una cadena codificada.

## <a name="remarks"></a>Comentarios

El BLOB devuelto contiene el contenido cifrado y una clave de sesión cifrada para cada destinatario previsto. Estas claves de sesión se cifran mediante la clave pública de cada destinatario. Las claves de sesión cifradas solo se pueden descifrar con la clave privada de un destinatario.

Si la [**propiedad Recipients**](envelopeddata-recipients.md) no contiene ninguna información, este método busca posibles destinatarios en el almacén de certificados AddressBook del usuario actual. Si se encuentra más de un destinatario potencial, se pide al usuario que seleccione un destinatario de un cuadro de diálogo de selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
