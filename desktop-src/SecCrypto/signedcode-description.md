---
description: Establece o recupera la descripción del archivo ejecutable firmado.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Propiedad SignedCode.Description
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
ms.openlocfilehash: 6046beae61aebaf33ea5eedb6ef2ec643f2edb39dbbedc61372085be2220068b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900355"
---
# <a name="signedcodedescription-property"></a>Propiedad SignedCode.Description

\[La **propiedad** Description está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API de Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad Description** establece o recupera la descripción del archivo ejecutable firmado.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Valor de propiedad

Descripción del archivo ejecutable firmado.

## <a name="remarks"></a>Comentarios

La descripción es el texto que aparece en el cuadro de diálogo Comprobación de Authenticode. El texto debe describir el archivo ejecutable firmado. Si esta propiedad es **NULL,** el cuadro de diálogo muestra el nombre del archivo ejecutable.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
