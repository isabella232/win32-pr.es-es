---
description: Establece el valor del secreto utilizado para derivar la clave de sesión criptográfica utilizada para cifrar y descifrar datos.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Método EncryptedData.SetSecret
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476430"
---
# <a name="encrypteddatasetsecret-method"></a>Método EncryptedData.SetSecret

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use Servicios de invocación de plataforma (PInvoke) para llamar a las funciones de API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar mensajes. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **método SetSecret** establece el valor del secreto utilizado para derivar la clave de [*sesión*](../secgloss/s-gly.md) criptográfica utilizada para cifrar y descifrar datos.

## <a name="syntax"></a>Sintaxis


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Cadena que contiene un secreto que se usa para crear una clave criptográfica de sesión.

</dd> <dt>

*SecretType* \[ en, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ SECRET \_ TYPE**](capicom-secret-type.md) que indica el tipo de secreto utilizado para generar la clave de sesión. El valor predeterminado es CAPICOM \_ SECRET \_ PASSWORD. Este parámetro puede ser el siguiente valor.



| Value                                                                                                                                                                                        | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**CONTRASEÑA SECRETA DE \_ \_ CAPICOM**</dt> </dl> | La clave de cifrado debe derivarse de una contraseña.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El secreto se usa para crear la clave de sesión para el cifrado o descifrado. Debe usarse el mismo secreto para ambas operaciones. Si se pierde el secreto usado para cifrar los datos, los datos cifrados no se pueden descifrar.

Si es adecuado para la aplicación, considere la posibilidad de usar [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger el secreto antes y después de su uso. Borre la memoria asociada al secreto cuando haya terminado.

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
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
