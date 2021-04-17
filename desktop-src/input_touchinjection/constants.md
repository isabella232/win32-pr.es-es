---
title: Constantes de inyección táctil
description: En esta sección se proporcionan las especificaciones de referencia para las constantes de inyección táctil.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 76a763a7153bbb9aa67254ffeb5e994a55426e43
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187738"
---
# <a name="touch-injection-constants"></a>Constantes de inyección táctil

En esta sección se proporcionan las especificaciones de referencia para las constantes de [inyección táctil](touch-injection-portal.md) .

| Constante o valor | Descripción |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Especifica el número máximo de contactos simultáneos.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Especifica visualizaciones táctiles predeterminadas.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0X2 | Especifica visualizaciones táctiles indirectas.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0X3             | No especifica ninguna visualización táctil.<br/>                     |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows 8 \[\]                                           |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2012 \[\]                                 |
| Encabezado                   | Winuser. h |

## <a name="see-also"></a>Consulte también

[Referencia de inyección táctil](touch-injection-reference.md)
