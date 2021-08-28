---
description: Representa información sobre un marco en la pila de llamadas.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631343"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>CallStackFrame (estructura)

Representa información sobre un marco en la pila de llamadas.

## <a name="syntax"></a>Sintaxis


```C++
} CallStackFrame;
```

## <a name="members"></a>Miembros

**Nombrefunción**  
Cadena COM que contiene el nombre de la función asociada.

**sourceFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen asociado.

**moduleName**  
Cadena COM que contiene el nombre del módulo de código asociado.

**lineNumber**  
Número de línea asociado.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



