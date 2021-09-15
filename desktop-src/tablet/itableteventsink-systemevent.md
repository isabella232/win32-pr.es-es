---
description: Se produce cuando hay disponible un evento del sistema.
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
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467976"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink::SystemEvent (método)

Se produce cuando hay disponible un evento del sistema.

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



 

## <a name="remarks"></a>Observaciones

La lista siguiente contiene los valores válidos para el parámetro de evento.

-   \_SE GRIFO
-   \_SE DBL \_ TAP
-   \_SE PULSAR \_ CON EL BOTÓN DERECHO
-   \_SE ARRASTRE
-   \_SE ARRASTRAR A \_ LA DERECHA
-   \_SE MANTENER \_ PRESIONADA LA TECLA ENTRAR
-   \_SE HOLD \_ LEAVE
-   \_SE MANTENGA EL \_ MOUSE SOBRE ENTRAR.
-   \_SE MANTENER EL \_ MOUSE SOBRE LA LICENCIA
-   \_SE MIDDLE \_ CLICK
-   \_SE CLAVE
-   \_SE TECLA \_ MODIFICADORA
-   \_SE MODO DE \_ GESTO
-   \_SE CURSOR

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 




