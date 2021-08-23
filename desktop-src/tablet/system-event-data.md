---
description: Contiene información sobre un evento del sistema de tabletas.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA estructura
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
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708215"
---
# <a name="system_event_data-structure"></a>Estructura DE \_ DATOS DE EVENTOS DEL \_ SISTEMA

Contiene información sobre un evento del sistema de tabletas.

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

Valores de bits para los modificadores. Consulte la sección de comentarios para obtener más información.

</dd> <dt>

**wKey**
</dt> <dd>

Examinar código para el carácter de teclado.

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

Tipo de cursor que produjo el evento. Consulte la sección de comentarios para obtener más información.

</dd> <dt>

**dwButtonState**
</dt> <dd>

Estado de los botones en el momento del evento del sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los siguientes eventos del sistema se definen para su uso en el **miembro bModifier.**



| Value               | Descripción                  |
|---------------------|------------------------------|
| \_SE MODIFICADOR \_ CTRL  | Se presionó la tecla Control. |
| \_SE MODIFICADOR \_ ALT   | Se presionó la tecla Alt.     |
| \_SE MODIFICADOR \_ MAYÚS | Se presionó la tecla Mayús.   |



 

Los siguientes eventos del sistema se definen para su uso en el **miembro bCursorMode.**



| Value              | Descripción               |
|--------------------|---------------------------|
| \_SE NORMAL \_ CURSOR | Indica la punta del lápiz.    |
| \_SE CURSOR \_ DE BORRADOR | Indica el borrador del lápiz. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStylusPlugin::SystemEvent (Método)**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink::SystemEvent (Método)**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




