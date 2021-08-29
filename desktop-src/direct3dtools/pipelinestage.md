---
description: Representa una fase de canalización, incluidos los detalles del sombreador utilizado.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PipeLineStage
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
ms.openlocfilehash: ecf25b450b613f433704de976d25fcbb77af8c7a586547fb99954a5cc86171e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119408"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Estructura PipeLineStage

Representa una fase de canalización, incluidos los detalles del sombreador utilizado.

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
Cadena COM que contiene el nombre del punto de entrada del sombreador, si lo hay.

**ShaderFile**  
Cadena COM que contiene la ruta de archivo del archivo de origen del sombreador.

**ShaderByteStreamPtr**  
FILEPTR para el flujo de bytes del sombreador. Esto se pasa de nuevo para depurar.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



