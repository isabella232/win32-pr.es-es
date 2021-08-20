---
description: Establece o recupera la dirección URL de una descripción del archivo ejecutable firmado.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Propiedad SignedCode.DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2668be4a9b0d4c6d746d0849c884c9819ad0d9291049e806e73fc1cea1b49d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974212"
---
# <a name="signedcodedescriptionurl-property"></a>Propiedad SignedCode.DescriptionURL

\[La **propiedad DescriptionURL** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API de Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad DescriptionURL** establece o recupera la dirección URL de una descripción del archivo ejecutable firmado.

## <a name="syntax"></a>Syntax


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Valor de propiedad

Dirección URL de una descripción del archivo ejecutable firmado.

## <a name="remarks"></a>Comentarios

**DescriptionURL es la** dirección URL a la que se vincula la [**descripción**](signedcode-description.md) que aparece en el cuadro de diálogo Comprobación de Authenticode. Si esta propiedad es **NULL,** **la descripción** no funciona como vínculo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
