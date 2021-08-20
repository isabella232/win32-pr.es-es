---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces.h)
description: Recibe una notificación que Windows Virtual PC registra un evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Equipo virtual del método OnEventLogged
- OnEventLogged method Virtual PC , IVMVirtualPCEvents interface
- IVMVirtualPCEvents interface Virtual PC , Método OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998525"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>IVMVirtualPCEvents::OnEventLogged (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe una notificación que Windows Virtual PC registra un evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*logMessageID* \[ En\]
</dt> <dd>

Identificador del mensaje del registro de eventos que se registró.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando Windows virtual registra un mensaje en el registro Windows eventos. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **\_ eventLogged vmVirtualPCEvent** que se origina en [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

