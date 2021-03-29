---
title: _aulldiv rutina)
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
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104487263"
---
# <a name="_aulldiv-routine"></a>\_Rutina aulldiv

Divide dos enteros **ULONGLONG** .
Por ejemplo, para dividir dos valores UInt64, el compilador puede generar una llamada a la rutina **\_ aulldiv** .

## <a name="remarks"></a>Observaciones

La rutina **\_ aulldiv** es una rutina auxiliar para el compilador de C.
Si el compilador usa **\_ aulldiv** depende completamente del conjunto de optimización.

Esta función solo se usa en plataformas x86.
