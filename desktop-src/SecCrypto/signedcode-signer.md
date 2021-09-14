---
description: Recupera el firmante del archivo ejecutable firmado.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Propiedad SignedCode.Signer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160724"
---
# <a name="signedcodesigner-property"></a>Propiedad SignedCode.Signer

\[La **propiedad Signer** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API de Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad Signer** recupera el firmante del archivo ejecutable firmado.

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**Signer**](signer.md) que proporciona acceso al firmante del archivo ejecutable firmado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
