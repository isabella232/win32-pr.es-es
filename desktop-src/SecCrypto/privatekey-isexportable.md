---
description: Devuelve un valor booleano que indica si la clave privada es exportable.
ms.assetid: 56e72747-126d-4bb4-ac10-ced0acef388b
title: Método PrivateKey.IsExportable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsExportable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e4056690be8661628baa1723583489375b37cbb69d2fc9340e218ece87a314b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978431"
---
# <a name="privatekeyisexportable-method"></a>Método PrivateKey.IsExportable

\[El **método IsExportable** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método IsExportable** devuelve un valor booleano que indica si la clave privada es exportable.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.IsExportable()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si es true, la clave privada se marca como exportable.

## <a name="remarks"></a>Comentarios

El valor devuelto de este método depende del proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado. Este método devolverá un valor de confianza si se usa un CSP de Microsoft. Si el CSP no es un CSP de Microsoft, no se puede confiar en que el valor devuelto sea preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
