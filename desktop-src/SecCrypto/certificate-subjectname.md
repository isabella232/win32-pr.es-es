---
description: Recupera una cadena que contiene el nombre del firmantes del certificado.
ms.assetid: 95dc7e8b-6670-4dfc-9fe1-d37635fb92d6
title: Propiedad Certificate.SubjectName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SubjectName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de38f1bbaf9af03eba8c026615eeb285c5a578002341a7c5023bf35a40e36f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878175"
---
# <a name="certificatesubjectname-property"></a>Propiedad Certificate.SubjectName

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad SubjectName** recupera una cadena que contiene el nombre del firmantes del certificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.SubjectName As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el nombre del sujeto del certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
