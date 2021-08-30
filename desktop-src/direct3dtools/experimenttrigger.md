---
description: Representa la información del desencadenador del experimento.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ExperimentTrigger (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ce4087e4e4ef30cedeb356730a0a7ae94252d4f3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625181"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger (estructura)

Representa la información del desencadenador del experimento.

## <a name="syntax"></a>Sintaxis


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Miembros

**type**  
Tipo de experimento (captura) desencadenado.

**key**  
Cuando type es igual a EXPERIMENTTRIGGERTYPE::KEY, la clave usada para desencadenar la captura.

**frameNumber**  
Cuando type es igual a EXPERIMENTTRIGGERTYPE::FRAMENUMBER, el número de fotograma que desencadenará la captura.

**captureCount**  
Número de fotogramas secuenciales que se capturan.

**actionIID**  
Identificador del evento de acción (captura de pantalla, captura de fotogramas, etc.).

**actionPlayload**  
Puntero a la carga del evento de acción.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



