---
description: Proporciona propiedades y métodos para cifrar y descifrar datos mediante una clave de sesión derivada de un secreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Objeto EncryptedData
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
ms.openlocfilehash: 15a66640ccdf794e88ae9cff04854a40fcfa6b763259da191bcdc6b07f11f449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874495"
---
# <a name="encrypteddata-object"></a>Objeto EncryptedData

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Servicios de invocación de plataforma (PInvoke) para llamar a las funciones de API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar mensajes. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **objeto EncryptedData** proporciona propiedades y métodos para cifrar y descifrar datos mediante una clave de [*sesión*](../secgloss/s-gly.md) derivada de un secreto.

> [!Note]  
> CAPICOM no admite el tipo de contenido PkCS 7 EncryptedData, pero usa una estructura ASN no estándar \# para **EncryptedData**. Por lo tanto, solo CAPICOM puede descifrar un objeto CAPICOM **EncryptedData.**

 

## <a name="members"></a>Miembros

El **objeto EncryptedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto EncryptedData** tiene estos métodos.



| Método                                       | Descripción                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Descifrar**](encrypteddata-decrypt.md)     | Descifra el contenido cifrado mediante el secreto.<br/>                                 |
| [**Encrypt**](encrypteddata-encrypt.md)     | Cifra el contenido mediante el secreto actual y el algoritmo de cifrado.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Establece el secreto del que se deriva la clave de sesión de cifrado y descifrado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto EncryptedData** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Solo lectura<br/>  | Algoritmo utilizado para el cifrado y descifrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Contenido**](encrypteddata-content.md)<br/>     | Lectura/escritura<br/> | Contenido que se va a cifrar o descifrar. El establecimiento de esta propiedad debe realizarse antes [**de llamar al**](encrypteddata-encrypt.md) método Encrypt. <br/> Cuando se restablece el valor de esta propiedad, [](../secgloss/s-gly.md) directa o indirectamente, se restablece todo el estado del objeto y se pierde cualquier contenido cifrado del objeto.<br/> Esta es la propiedad predeterminada.<br/> |



 

## <a name="remarks"></a>Comentarios

Se puede crear el objeto **EncryptedData** y es seguro para el scripting. El ProgID del **objeto EncryptedData** es CAPICOM. EncryptedData.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
