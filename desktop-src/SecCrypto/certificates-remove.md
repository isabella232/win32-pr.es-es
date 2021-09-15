---
description: Quita un único objeto Certificate de la colección.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: ICertificates2::Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271188"
---
# <a name="icertificates2remove-method"></a>ICertificates2::Remove (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Remove** quita un único objeto [**Certificate**](certificate.md) de la colección. Este método se introdujo en CAPICOM 2.0.

## <a name="syntax"></a>Sintaxis


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Valor de índice para el [**objeto Certificate**](certificate.md) que se va a quitar. Este parámetro puede ser uno de los siguientes tipos posibles.



| Tipo                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>**Long***</dt><dt></dt> </dl>                                                | Se [**quita**](certificate.md) el objeto Certificate en el índice especificado de la colección.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**String***</dt><dt></dt> </dl>                                        | Se quita [**el primer**](certificate.md) objeto Certificate de la colección que coincide con la huella digital [*SHA-1*](../secgloss/s-gly.md) contenida en la cadena especificada.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Certificado**](certificate.md)**</dt><dt></dt> </dl> | Se quita [**el primer objeto Certificate**](certificate.md) de la colección que coincida con el objeto **Certificate** especificado.<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
