---
title: _allmul rutina)
description: Multiplica dos enteros de LONGLONG o ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104077229"
---
# <a name="_allmul-routine"></a>\_Rutina allmul

Multiplica dos enteros de **LONGLONG** o **ULONGLONG** .
Por ejemplo, para multiplicar dos valores Int64, el compilador puede generar una llamada a la rutina **\_ allmul** .

## <a name="remarks"></a>Observaciones

La rutina **\_ allmul** es una rutina auxiliar para el compilador de C.
Si el compilador usa **\_ allmul** depende completamente del conjunto de optimización.

Esta rutina solo se usa en plataformas x86.
