---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Recibe la notificación de que Windows Virtual PC registra un evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Método OnEventLogged Virtual PC
- Método OnEventLogged Virtual PC, interfaz IVMVirtualPCEvents
- Interfaz IVMVirtualPCEvents Virtual PC, método OnEventLogged
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
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534390"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>IVMVirtualPCEvents:: OnEventLogged (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recibe la notificación de que Windows Virtual PC registra un evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*logMessageID* \[ de\]
</dt> <dd>

Identificador de mensaje del mensaje de registro de eventos que se registró.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cuando Windows Virtual PC registra un mensaje en el registro de eventos de Windows. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualPCEvent \_ EventLogged** que se origina desde [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

