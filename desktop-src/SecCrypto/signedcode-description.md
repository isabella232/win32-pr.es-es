---
description: Establece o recupera la descripción del archivo ejecutable firmado.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: SignedCode. Description (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671093"
---
# <a name="signedcodedescription-property"></a>SignedCode. Description (propiedad)

\[La propiedad **Description** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

La propiedad **Description** establece o recupera la descripción del archivo ejecutable firmado.

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Valor de propiedad

La descripción del archivo ejecutable firmado.

## <a name="remarks"></a>Observaciones

La descripción es el texto que aparece en el cuadro de diálogo Comprobación de Authenticode. El texto debe describir el archivo ejecutable firmado. Si esta propiedad es **null**, el cuadro de diálogo muestra el nombre del archivo ejecutable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
