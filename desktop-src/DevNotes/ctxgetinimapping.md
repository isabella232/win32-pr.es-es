---
description: Determina si el Terminal Server está en modo de instalación (solo en Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650077"
---
# <a name="ctxgetinimapping-function"></a>CtxGetIniMapping función)

\[Esta función no se admite y no debe usarse. Puede cambiar o desaparecer por completo sin aviso previo. En su lugar, use **VerifyVersionInfo**.\]

Determina si el Terminal Server está en modo de instalación (solo en Windows Terminal Server 4,0).

## <a name="syntax"></a>Sintaxis


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **false** si el Terminal Server está en modo de instalación, es **true** si está en modo de ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
