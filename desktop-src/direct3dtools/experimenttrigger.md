---
description: Representa la información del desencadenador del experimento.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura ExperimentTrigger
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
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906564"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>Estructura ExperimentTrigger

Representa la información del desencadenador del experimento.

## <a name="syntax"></a>Sintaxis


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Miembros

**type**  
El tipo de experimento (captura) desencadenado.

**key**  
Cuando el tipo es igual a EXPERIMENTTRIGGERTYPE:: KEY, la clave utilizada para desencadenar la captura.

**Númeromarco**  
Cuando el tipo es igual a EXPERIMENTTRIGGERTYPE:: NÚMEROMARCO, el número de marco que desencadenará la captura.

**captureCount**  
Número de fotogramas secuenciales que se van a capturar.

**actionIID**  
IDENTIFICADOR del evento de acción (captura de pantalla, captura de fotogramas, etc.).

**actionPlayload**  
Puntero a la carga del evento de acción.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



