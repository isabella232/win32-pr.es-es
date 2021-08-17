---
description: Devuelve una colección de las extensiones asociadas al certificado.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: ICertificate2::Extensions (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e700fda2fb99e0ea0a3dfd8690fdfedbdeecb21bc84bfdb08cbf1f179536cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771617"
---
# <a name="icertificate2extensions-method"></a>ICertificate2::Extensions (Método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Extensions** devuelve una colección de las extensiones asociadas al certificado. Este método se introdujo en CAPICOM 2.0.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.Extensions()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Objeto [**Extensions**](extensions.md) que representa todas las extensiones asociadas al certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
