---
description: Las constantes de marca de bits LINECALLPRIVILEGE describen los tipos de derechos de acceso o privilegios que puede tener una aplicación con un identificador de llamada \_ a la llamada correspondiente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c00dd43442345c545bb5e0b1718131b6815fd236f9c7d770c0f3b47b10b47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660055"
---
# <a name="linecallprivilege_-constants"></a>LineCALLPRIVILEGE \_ (Constantes)

Las constantes de marca de bits **LINECALLPRIVILEGE \_** describen los tipos de derechos de acceso o privilegios que puede tener una aplicación con un identificador de llamada a la llamada correspondiente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE \_ MONITOR**
</dt> <dd> <dl> <dt>



La aplicación tiene privilegios de supervisión para la llamada. Estos privilegios permiten a la aplicación supervisar los cambios de estado y consultar información y estado sobre la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ NONE**
</dt> <dd> <dl> <dt>



La aplicación no tiene privilegios para la llamada. El identificador de la aplicación es void y no se debe usar.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE \_ OWNER**
</dt> <dd> <dl> <dt>



La aplicación tiene privilegios de propietario para la llamada. Estos privilegios permiten a la aplicación manipular la llamada de maneras que afectan al estado de la llamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Cuando se proporciona por primera vez un identificador de llamada a una aplicación o cada vez que se modifican los privilegios de llamada de esa aplicación, el mensaje [**LINE \_ CALLSTATE**](line-callstate.md) se envía a la aplicación. Cuando una aplicación realiza una llamada y la aplicación receptora aún no tiene un identificador con privilegios de propietario, este mensaje informa a la aplicación sobre sus nuevos privilegios para la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




