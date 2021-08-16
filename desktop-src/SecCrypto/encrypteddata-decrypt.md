---
description: Descifra una cadena de datos cifrada y codificada.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Método EncryptedData.Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8bf8a108efdc462a9f08a508a05b736817ec38ce43ee50dbd3fdd11aa2af9f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766712"
---
# <a name="encrypteddatadecrypt-method"></a>Método EncryptedData.Decrypt

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Platform Invocation Services (PInvoke) para llamar a las funciones de API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar mensajes. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **método Decrypt** descifra una cadena de datos cifrada y codificada. Los datos de texto no cifrado resultantes se [**convierten en la propiedad Content**](encrypteddata-content.md) del objeto [**EncryptedData.**](encrypteddata.md) Se produce un error de descifrado del contenido a menos que el secreto, establecido por el [**método SetSecret,**](encrypteddata-setsecret.md) sea exactamente el mismo que el secreto utilizado para derivar la clave utilizada para cifrar el contenido.

## <a name="syntax"></a>Sintaxis


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncryptedMessage* \[ En\]
</dt> <dd>

Cadena que contiene los datos cifrados codificados que se descifrarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La clave de sesión derivada del secreto actual se usa para el descifrado. Este método no producirá el texto no cifrado correcto a menos que el secreto actual coincida exactamente con el secreto utilizado para cifrar el mensaje.

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

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
