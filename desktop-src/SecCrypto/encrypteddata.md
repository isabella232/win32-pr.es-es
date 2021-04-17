---
description: Proporciona propiedades y métodos para cifrar y descifrar datos mediante una clave de sesión derivada de un secreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: EncryptedData (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670439"
---
# <a name="encrypteddata-object"></a>EncryptedData (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El objeto **EncryptedData** proporciona propiedades y métodos para cifrar y descifrar los datos mediante una [*clave de sesión*](../secgloss/s-gly.md) derivada de un secreto.

> [!Note]  
> CAPICOM no admite el tipo de \# contenido de PKCS 7 EncryptedData, pero usa una estructura ASN no estándar para **EncryptedData**. Por lo tanto, solo CAPICOM puede descifrar un objeto **EncryptedData** de CAPICOM.

 

## <a name="members"></a>Miembros

El objeto **EncryptedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **EncryptedData** tiene estos métodos.



| Método                                       | Descripción                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Descifrado**](encrypteddata-decrypt.md)     | Descifra el contenido cifrado mediante el secreto.<br/>                                 |
| [**Cifrado**](encrypteddata-encrypt.md)     | Cifra el contenido con el algoritmo de cifrado y secreto actual.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Establece el secreto del que se deriva la clave de sesión de cifrado/descifrado.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **EncryptedData** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Solo lectura<br/>  | Algoritmo usado para el cifrado y el descifrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Contenido**](encrypteddata-content.md)<br/>     | Lectura/escritura<br/> | Contenido que se va a cifrar o descifrar. La configuración de esta propiedad debe realizarse antes de llamar al método de [**cifrado**](encrypteddata-encrypt.md) . <br/> Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier contenido cifrado en el objeto.<br/> Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **EncryptedData** y es seguro para el scripting. El ProgID del objeto **EncryptedData** es CAPICOM. EncryptedData. 1.

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
</dt> </dl>

 

 
