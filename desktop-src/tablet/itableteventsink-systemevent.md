---
description: Se produce cuando hay un evento del sistema disponible.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'ITabletEventSink:: SystemEvent (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648509"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink:: SystemEvent (método)

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

*TCID* \[ de\]
</dt> <dd>

El identificador de la tableta.

</dd> <dt>

*CID* \[ en\]
</dt> <dd>

Identificador del lápiz óptico.

</dd> <dt>

*evento* \[ de de\]
</dt> <dd>

Código de evento del sistema.

</dd> <dt>

*EventData* \[ de\]
</dt> <dd>

Datos de eventos del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

La lista siguiente contiene los valores válidos para el parámetro de evento.

-   SE \_ TAP
-   SE \_ \_ TAP doble
-   SE \_ \_ TAP derecho
-   SE ha \_ arrastrado
-   SE \_ arrastra a la derecha \_
-   SE \_ mantiene presionado \_ entrar
-   SE \_ mantiene presionado \_
-   SE \_ mantiene el mouse \_ Enter
-   mantener el \_ mouse en \_ salir
-   SE \_ hace clic con el botón \_
-   \_tecla se
-   \_tecla modificador \_ se
-   \_modo de gestos de se \_
-   \_cursor se

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




