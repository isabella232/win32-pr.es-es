---
description: Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad SignedCode.FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Método SignedCode.Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160726"
---
# <a name="signedcodesign-method"></a>Método SignedCode.Sign

\[El **método Sign** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use Platform Invocation Services (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **método Sign** crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad [**SignedCode.FileName.**](signedcode-filename.md)

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Firmante* \[ in, opcional\]
</dt> <dd>

Objeto [**Signer**](signer.md) que tiene acceso a la clave privada del certificado que se usa para firmar el código. El valor predeterminado es **Null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar al método **Sign,** el archivo que contiene el código debe especificarse en la [**propiedad FileName.**](signedcode-filename.md)

Si el archivo ejecutable ya está firmado, este método sobrescribe la firma existente.

Los resultados siguientes se aplican al valor del parámetro *Signer:*

-   Si el *parámetro Signer* no es **NULL,** este método usa la clave privada a la que apunta el certificado asociado para cifrar la firma. Si la clave privada a la que apunta el certificado no está disponible, se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y hay exactamente un certificado en el almacén CURRENT USER MY que tiene acceso a una clave privada con funcionalidad de firma de código, ese certificado se usa para crear \_ la firma.
-   Si el *parámetro Signer* es **NULL**, el [**Configuración. El**](settings-enablepromptforcertificateui.md) valor de la propiedad EnablePromptForCertificateUI es true y hay más de un certificado en el almacén MI USUARIO ACTUAL con una clave privada disponible con la funcionalidad de firma de código, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se \_ usa.
-   Si el *parámetro Signer* es **NULL** y el [**Configuración. La propiedad EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false y se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y no hay ningún certificado en el almacén CURRENT USER MY con una clave privada disponible con la funcionalidad de firma de código, se produce un \_ error en el método.

Este método usa el algoritmo hash SHA-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
