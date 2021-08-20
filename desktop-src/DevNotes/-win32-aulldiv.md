---
title: _aulldiv rutina
description: Divide dos enteros ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538905"
---
# <a name="_aulldiv-routine"></a>\_aulldiv (rutina)

Divide dos **enteros ULONGLONG.**
Por ejemplo, para dividir dos valores uint64, el compilador podría generar una llamada a la **\_ rutina aulldiv.**

## <a name="remarks"></a>Comentarios

La **\_ rutina aulldiv** es una rutina auxiliar para el compilador de C.
Si el compilador usa **\_ aulldiv** depende completamente del conjunto de optimización.

Esta función solo se usa en plataformas x86.
