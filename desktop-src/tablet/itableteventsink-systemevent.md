---
description: Se produce cuando hay un evento del sistema disponible.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: ITabletEventSink::SystemEvent (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 6d2e636b5e0b70d13ae33850518e744fbc9425bd65c20002a89b6d38e56dbc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041751"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink::SystemEvent (método)

Se produce cuando hay un evento del sistema disponible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tcid* \[ En\]
</dt> <dd>

Identificador de la tableta.

</dd> <dt>

*cid* \[ en\]
</dt> <dd>

Identificador del lápiz óptico.

</dd> <dt>

*evento* \[ En\]
</dt> <dd>

Código de evento del sistema.

</dd> <dt>

*eventdata* \[ En\]
</dt> <dd>

Datos de eventos del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

La lista siguiente contiene los valores válidos para el parámetro de evento.

-   \_SE Grifo
-   \_SE DBL \_ TAP
-   \_SE PULSAR \_ CON EL BOTÓN DERECHO
-   \_SE Arrastre
-   \_SE ARRASTRAR \_ A LA DERECHA
-   \_SE MANTENER \_ PRESIONADA LA TECLA ENTRAR
-   \_SE HOLD \_ LEAVE
-   \_SE MANTENER EL \_ PUNTERO SOBRE ENTRAR
-   \_SE MANTENER EL \_ MOUSE SOBRE SALIR
-   \_SE MIDDLE \_ CLICK
-   \_SE Clave
-   \_SE TECLA \_ MODIFICADORA
-   \_SE MODO \_ GESTO
-   \_SE Cursor

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 




