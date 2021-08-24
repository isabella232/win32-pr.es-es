---
description: Determina si Terminal Server está en modo INSTALL (solo en Terminal Windows Server 4.0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Función CtxGetIniMapping
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
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654215"
---
# <a name="ctxgetinimapping-function"></a>Función CtxGetIniMapping

\[Esta función no se admite y no se debe usar. Puede cambiar o desaparecer completamente sin previo aviso. En su lugar, use **VerifyVersionInfo**.\]

Determina si Terminal Server está en modo INSTALL (solo en Terminal Windows Server 4.0).

## <a name="syntax"></a>Sintaxis


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **FALSE si** Terminal Server está en modo INSTALL, **TRUE** si está en modo EXECUTE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
