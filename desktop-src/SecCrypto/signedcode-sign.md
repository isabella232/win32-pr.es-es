---
description: Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690757"
---
# <a name="signedcodesign-method"></a>SignedCode. Sign (método)

\[El método **Sign** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El método **Sign** crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Firmante* \[ en, opcional\]
</dt> <dd>

Objeto de [**firmante**](signer.md) que tiene acceso a la clave privada del certificado utilizado para firmar el código. El valor predeterminado es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar al método **Sign** , el archivo que contiene el código debe especificarse en la propiedad [**filename**](signedcode-filename.md) .

Si el archivo ejecutable ya está firmado, este método sobrescribe la firma existente.

Los resultados siguientes se aplican al valor del parámetro *Signer* :

-   Si el parámetro del *firmante* no es **null**, este método utiliza la clave privada a la que apunta el certificado asociado para cifrar la firma. Si no está disponible la clave privada a la que apunta el certificado, se produce un error en el método.
-   Si el parámetro de *firmante* es **null** y hay exactamente un certificado en el usuario actual \_ mi almacén que tiene acceso a una clave privada con la funcionalidad de firma de código, ese certificado se usa para crear la firma.
-   Si el parámetro de *firmante* es **null**, el valor de la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es true y hay más de un certificado en el \_ usuario actual My Store con una clave privada disponible con la funcionalidad de firma de código, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se usa.
-   Si el parámetro de *firmante* es **null** y la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false, se produce un error en el método.
-   Si el parámetro del *firmante* es **null** y no hay ningún certificado en el \_ almacén del usuario actual con una clave privada disponible con la funcionalidad de firma de código, se produce un error en el método.

Este método usa el algoritmo hash SHA-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
