---
description: Los \_ valores de enumeración de Estados de la operación de WPD \_ describen el estado actual de una operación en curso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumeración WPD_OPERATION_STATES (PortableDevice. h)
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
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699964"
---
# <a name="wpd_operation_states-enumeration"></a>\_Enumeración de Estados de operación de WPD \_

Los valores de enumeración de **\_ \_ Estados** de la operación de WPD describen el estado actual de una operación en curso.

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

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**Estado de la operación de WPD no \_ \_ \_ especificado**
</dt> <dd>

La operación actual está en un estado no especificado (no establecido) y se desconoce.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**Estado de la operación de WPD \_ \_ \_ iniciado**
</dt> <dd>

La operación se ha iniciado.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**Estado de la operación de WPD en \_ \_ \_ ejecución**
</dt> <dd>

La operación se está ejecutando.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**Estado de la operación de WPD en \_ \_ \_ pausa**
</dt> <dd>

La operación está en pausa.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**Estado de operación de WPD \_ \_ \_ cancelado**
</dt> <dd>

La operación se cancela.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**Estado de la operación de WPD \_ \_ \_ finalizado**
</dt> <dd>

La operación ha finalizado.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**Estado de operación de WPD \_ \_ \_ anulado**
</dt> <dd>

La operación se ha anulado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos valores se reciben en la devolución de llamada definida por la aplicación ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




