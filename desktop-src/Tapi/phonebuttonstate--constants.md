---
description: Las constantes de marca de bits PHONEBUTTONSTATE describen las posiciones de los botones.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: PHONEBUTTONSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95070eb24b5189b44f07a8ba2d2d7ed7d8234ec14a97889f09c0fe29ac72eed9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100515"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ constantes

Las **PHONEBUTTONSTATE_** de marca de bits describen las posiciones del botón.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



El botón está en estado "abajo" (presionado).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios no conoce el estado de arriba o abajo del botón y que no se conocerá en un momento futuro. (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indica que el estado de arriba o abajo del botón no se conoce en este momento, pero puede conocerse en un momento futuro. (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



El botón está en estado "up".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión negociada de la API en el teléfono y no usar esos valores PHONEBUTTONSTATE_ que la versión negociada no admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




