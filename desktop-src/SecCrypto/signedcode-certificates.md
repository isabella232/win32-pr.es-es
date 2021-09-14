---
description: Recupera la colección de certificados en el archivo ejecutable firmado.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Propiedad SignedCode.Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173118"
---
# <a name="signedcodecertificates-property"></a>Propiedad SignedCode.Certificates

\[La **propiedad Certificados** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API de Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

La **propiedad Certificates** recupera la colección de certificados en el archivo ejecutable firmado.

## <a name="syntax"></a>Sintaxis


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a>Valor de propiedad

Colección [**Certificates**](certificates.md) que contiene todos los certificados del archivo ejecutable firmado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
