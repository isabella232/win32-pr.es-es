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
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997799"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Estructura PipeLineStage

Representa una fase de canalización, incluidos los detalles del sombreador utilizado.

## <a name="syntax"></a>Sintaxis


```C++
} PipeLineStage;
```

## <a name="members"></a>Miembros

**StageId**  
IDENTIFICADOR de la fase de canalización.

**Depurable**  
True si la fase de canalización admite la depuración; en caso contrario, false.

**StageName**  
Cadena COM que contiene el nombre de la fase de canalización.

**GuaranteedOutput**  
True si la fase de canalización siempre tiene una salida de canalización; en caso contrario, false.

**DebugEntryPoint**  
Cadena COM que contiene el nombre del punto de entrada del sombreador, si hay alguno.

**ShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador.

**ShaderByteStreamPtr**  
Un FILEPTR para la secuencia de bytes del sombreador. Esto se devuelve para depurar.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



