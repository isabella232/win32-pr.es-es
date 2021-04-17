---
description: Crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. timestamp (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690375"
---
# <a name="signedcodetimestamp-method"></a>SignedCode. timestamp (método)

\[El método **timestamp** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El método **timestamp** crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad **SignedCode. FileName** . Esta marca de tiempo es una firma de contador en el archivo ejecutable firmado que realiza una autoridad de marca de tiempo.

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

Cadena que contiene la dirección URL del servidor de marca de tiempo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una marca de tiempo amplía la validez de un certificado comprobando que el archivo ejecutable se firmó en el momento en que se realizó la marca de tiempo.

Antes de que se pueda llamar a este método, se debe especificar el archivo ejecutable firmado para marca de tiempo en la propiedad **SignedCode. FileName** y se debe llamar al método [**SignedCode. Sign**](signedcode-sign.md) para firmar el archivo ejecutable.

Si el archivo ejecutable firmado ya tiene una marca de tiempo, este método sobrescribe la marca de tiempo existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
