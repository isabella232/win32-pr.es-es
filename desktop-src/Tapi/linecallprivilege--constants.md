---
description: Las \_ constantes de marcador de bits LINECALLPRIVILEGE describen los tipos de derechos de acceso o los privilegios que una aplicación con un identificador de llamada puede tener en la llamada correspondiente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes de LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681089"
---
# <a name="linecallprivilege_-constants"></a>Constantes de LINECALLPRIVILEGE \_

Las constantes de marcador de bits **LINECALLPRIVILEGE \_** describen los tipos de derechos de acceso o los privilegios que una aplicación con un identificador de llamada puede tener en la llamada correspondiente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**MONITOR de LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



La aplicación tiene privilegios de supervisión para la llamada. Estos privilegios permiten a la aplicación supervisar los cambios de estado y la información de consulta y el estado de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ ninguno**
</dt> <dd> <dl> <dt>



La aplicación no tiene privilegios para la llamada. El identificador de la aplicación es nulo y no debe usarse.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**propietario de LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



La aplicación tiene privilegios de propietario en la llamada. Estos privilegios permiten a la aplicación manipular la llamada de maneras que afectan al estado de la llamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Cuando un identificador de llamada se proporciona por primera vez a una aplicación o cuando se modifican los privilegios de llamada de esa aplicación, el mensaje de [**línea \_ CALLSTATE**](line-callstate.md) se envía a la aplicación. Cuando una aplicación hace una llamada a, y si la aplicación receptora todavía no tiene un identificador con privilegios de propietario, este mensaje informa a la aplicación sobre sus nuevos privilegios a la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




