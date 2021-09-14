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
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173114"
---
# <a name="signedcodedescriptionurl-property"></a>Propiedad SignedCode.DescriptionURL

\[La **propiedad DescriptionURL** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use Platform Invocation Services (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad DescriptionURL** establece o recupera la dirección URL de una descripción del archivo ejecutable firmado.

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Valor de propiedad

Dirección URL de una descripción del archivo ejecutable firmado.

## <a name="remarks"></a>Observaciones

**DescriptionURL es la** dirección URL a la que se vincula la [**descripción**](signedcode-description.md) que aparece en el cuadro de diálogo Comprobación de Authenticode. Si esta propiedad es **NULL**, **la descripción** no funciona como vínculo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
