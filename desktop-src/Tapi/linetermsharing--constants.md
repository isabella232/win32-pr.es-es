---
description: Las \_ constantes de marcador de bits LINETERMSHARING describen diferentes formas en que un terminal puede compartirse entre dispositivos de línea, direcciones o llamadas.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes de LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690258"
---
# <a name="linetermsharing_-constants"></a>Constantes de LINETERMSHARING \_

Las constantes de marcador de bits **LINETERMSHARING \_** describen diferentes formas en que un terminal puede compartirse entre dispositivos de línea, direcciones o llamadas.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privado**
</dt> <dd> <dl> <dt>



El dispositivo terminal es privado para un dispositivo de una sola línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**
</dt> <dd> <dl> <dt>



El dispositivo terminal se puede usar en varias líneas. Las solicitudes de [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) de los distintos terminales finalizan su combinación o conferencia en el terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**
</dt> <dd> <dl> <dt>



El dispositivo terminal se puede usar en varias líneas. El dispositivo de última línea para realizar una [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) o [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) en el terminal para un modo de terminal determinado tendrá una conexión exclusiva con el terminal para ese modo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Estas constantes describen las clases de secuencias de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo de terminal (como un conjunto de teléfonos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

