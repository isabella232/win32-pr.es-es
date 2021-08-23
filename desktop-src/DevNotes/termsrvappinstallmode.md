---
description: Determina si Terminal Server está en modo INSTALL.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Función TermsrvAppInstallMode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f6bf6408fb7bd72b1757b8ca2219e1bbd2cc612829359fdcaf090786e8e7e98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570895"
---
# <a name="termsrvappinstallmode-function"></a>Función TermsrvAppInstallMode

\[Esta función no se admite y no se debe usar. Puede cambiar o desaparecer completamente sin previo aviso.\]

Determina si Terminal Server está en modo INSTALL.

## <a name="syntax"></a>Sintaxis


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** Terminal Server está en modo INSTALL y **FALSE** si está en modo EXECUTE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




