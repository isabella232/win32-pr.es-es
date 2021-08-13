---
description: Los valores de \_ enumeración WPD OPERATION \_ STATES describen el estado actual de una operación en curso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: WPD_OPERATION_STATES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3c2bc25fdbc040bd849d60f1e16e5d86d1916ced17eb6670ceb3bc6a75108772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696488"
---
# <a name="wpd_operation_states-enumeration"></a>Enumeración \_ WPD OPERATION \_ STATES

Los **valores de \_ enumeración WPD OPERATION \_ STATES** describen el estado actual de una operación en curso.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**ESTADO DE \_ LA OPERACIÓN \_ WPD SIN \_ ESPECIFICAR**
</dt> <dd>

La operación actual está en un estado no especificado (no establecido) y desconocido.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**ESTADO DE LA \_ OPERACIÓN \_ WPD \_ INICIADA**
</dt> <dd>

Se inicia la operación.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD \_ OPERATION \_ STATE \_ RUNNING**
</dt> <dd>

La operación se está ejecutando.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**ESTADO DE \_ LA OPERACIÓN \_ \_ WPD EN PAUSA**
</dt> <dd>

La operación está en pausa.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**ESTADO DE \_ LA OPERACIÓN \_ WPD \_ CANCELADA**
</dt> <dd>

La operación se cancela.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**ESTADO DE LA \_ OPERACIÓN \_ WPD \_ FINALIZADA**
</dt> <dd>

La operación ha finalizado.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**ESTADO DE \_ LA OPERACIÓN \_ WPD \_ ANULADA**
</dt> <dd>

Se anula la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos valores se reciben en la devolución de llamada definida por la aplicación ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




