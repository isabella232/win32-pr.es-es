---
description: Contiene información acerca de un evento de Tablet PC.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Estructura de SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279379"
---
# <a name="system_event_data-structure"></a>Estructura de datos de \_ eventos del sistema \_

Contiene información acerca de un evento de Tablet PC.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**bModifier**
</dt> <dd>

Valores de bit para los modificadores. Vea la sección Comentarios para obtener más información.

</dd> <dt>

**wKey**
</dt> <dd>

Digitalice el código para el carácter del teclado.

</dd> <dt>

**xPos**
</dt> <dd>

Posición X del evento.

</dd> <dt>

**yPos**
</dt> <dd>

Posición Y del evento.

</dd> <dt>

**bCursorMode**
</dt> <dd>

El tipo de cursor que causó el evento. Vea la sección Comentarios para obtener más información.

</dd> <dt>

**dwButtonState**
</dt> <dd>

Estado de los botones en el momento del evento del sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los siguientes eventos del sistema se definen para su uso en el miembro **bModifier** .



| Value               | Descripción                  |
|---------------------|------------------------------|
| SE \_ modificador se \_ Ctrl  | Se presionó la tecla control. |
| \_modificador se \_ Alt Alt   | Se presionó la tecla Alt.     |
| \_desplazamiento del modificador se \_ | Se presionó la tecla Mayús.   |



 

Los siguientes eventos del sistema se definen para su uso en el miembro **bCursorMode** .



| Value              | Descripción               |
|--------------------|---------------------------|
| \_cursor normal de se \_ | Indica la punta del lápiz.    |
| \_cursor de borrador de se \_ | Indica el borrador del lápiz. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStylusPlugin:: SystemEvent (método)**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink:: SystemEvent (método)**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




