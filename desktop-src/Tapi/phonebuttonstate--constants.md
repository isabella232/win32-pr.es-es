---
description: Las constantes de marcador de bits PHONEBUTTONSTATE describen las posiciones de los botones.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes de PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691111"
---
# <a name="phonebuttonstate_-constants"></a>Constantes de PHONEBUTTONSTATE_

Las constantes de marcador de bits **PHONEBUTTONSTATE_** describen las posiciones del botón.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



El botón está en el estado "inactivo" (presionado).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios no conoce el estado activo o inactivo del botón y que no se conocerá en el futuro. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Indica que en este momento no se conoce el estado arriba o abajo del botón, pero se puede conocer en el futuro. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



El botón está en el estado "activo".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en el teléfono y no utilizar los valores de PHONEBUTTONSTATE_ que la versión negociada no admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




