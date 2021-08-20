---
description: Las constantes de marca de bits LINETERMSHARING describen distintas maneras de compartir un terminal entre \_ dispositivos de línea, direcciones o llamadas.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: LINETERMSHARING_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0465899b8875545d70419f0892b57f10b8c1dce16256890f8b384817d6094108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944852"
---
# <a name="linetermsharing_-constants"></a>Constantes LINETERMSHARING \_

Las constantes de marca de bits **LINETERMSHARING \_** describen distintas maneras de compartir un terminal entre dispositivos de línea, direcciones o llamadas.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ PRIVATE**
</dt> <dd> <dl> <dt>



El dispositivo terminal es privado para un dispositivo de una sola línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**
</dt> <dd> <dl> <dt>



El dispositivo terminal se puede usar en varias líneas. Las [**solicitudes lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) de los distintos terminales terminan fusionadas o con conferencias en el terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**
</dt> <dd> <dl> <dt>



El dispositivo terminal se puede usar en varias líneas. El último dispositivo de línea que va a realizar un [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) o [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) en el terminal para un modo de terminal determinado tendrá una conexión exclusiva al terminal para ese modo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Estas constantes describen las clases de flujos de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo terminal (por ejemplo, un conjunto de teléfonos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

