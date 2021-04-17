---
description: Establece el valor del secreto que se usa para derivar la clave de sesión criptográfica usada para cifrar y descifrar los datos.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. SetSecret (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670440"
---
# <a name="encrypteddatasetsecret-method"></a>EncryptedData. SetSecret (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El método **SetSecret** establece el valor del secreto que se usa para derivar la [*clave de sesión*](../secgloss/s-gly.md) criptográfica usada para cifrar y descifrar los datos.

## <a name="syntax"></a>Sintaxis


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Cadena que contiene un secreto que se usa para crear una clave criptográfica de sesión.

</dd> <dt>

*SecretType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo de secreto de CAPICOM**](capicom-secret-type.md) que indica el tipo de secreto usado para generar la clave de sesión. El valor predeterminado es la \_ contraseña del secreto de CAPICOM \_ . Este parámetro puede ser el valor siguiente.



| Value                                                                                                                                                                                        | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**\_contraseña secreta de CAPICOM \_**</dt> </dl> | La clave de cifrado debe derivarse de una contraseña.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El secreto se usa para crear la clave de sesión para el cifrado o descifrado. Se debe usar el mismo secreto para ambas operaciones. Si se pierde el secreto que se usa para cifrar los datos, los datos cifrados no se pueden descifrar.

Si es adecuado para su aplicación, considere la posibilidad de usar [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger el secreto antes y después de usarlo. Borre la memoria asociada al secreto cuando haya terminado.

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

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
