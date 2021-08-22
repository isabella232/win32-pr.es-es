---
title: Constantes de inserción táctil
description: En esta sección se proporcionan las especificaciones de referencia para las constantes de inserción táctil.
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
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451745"
---
# <a name="touch-injection-constants"></a>Constantes de inserción táctil

En esta sección se proporcionan las especificaciones de referencia para [las constantes de inserción](touch-injection-portal.md) táctil.

| Constante o valor | Descripción |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Especifica el número máximo de contactos simultáneos.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Especifica visualizaciones táctiles predeterminadas.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | Especifica visualizaciones táctiles indirectas.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | No especifica visualizaciones táctiles.<br/>                     |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible | \[Windows 8 solo aplicaciones de escritorio\]                                           |
| Servidor mínimo compatible | \[Windows Server 2012 solo aplicaciones de escritorio\]                                 |
| Header                   | Winuser.h |

## <a name="see-also"></a>Vea también

[Referencia de inserción táctil](touch-injection-reference.md)
