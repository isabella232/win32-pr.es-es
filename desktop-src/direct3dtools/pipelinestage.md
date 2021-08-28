---
description: Representa una fase de canalización, incluidos los detalles del sombreador usado.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625171"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>PipeLineStage (estructura)

Representa una fase de canalización, incluidos los detalles del sombreador usado.

## <a name="syntax"></a>Sintaxis


```C++
} PipeLineStage;
```

## <a name="members"></a>Miembros

**StageId**  
Identificador de la fase de canalización.

**Depurable**  
true si la fase de canalización admite la depuración; de lo contrario, false.

**StageName**  
Cadena COM que contiene el nombre de la fase de canalización.

**GuaranteedOutput**  
True si la fase de canalización siempre tiene salida de canalización; de lo contrario, false.

**DebugEntryPoint**  
Cadena COM que contiene el nombre del punto de entrada del sombreador, si hay uno.

**ShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador.

**ShaderByteStreamPtr**  
FILEPTR para la secuencia de bytes del sombreador. Esto se pasa de nuevo para depurar.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



