---
title: Método IVMTask WaitForCompletion (VPCCOMInterfaces.h)
description: Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Equipo virtual del método WaitForCompletion
- Método WaitForCompletion De PC virtual, interfaz IVMTask
- IVMTask interface Virtual PC , Método WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd77019c98e48f4707ac173f825823d5637a1d83c5eb1583f4ee68874e84bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752706"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask::WaitForCompletion (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tiempo de espera* \[ En\]
</dt> <dd>

Tiempo, en milisegundos, que este método esperará a que finalice la tarea antes de devolver el control al autor de la llamada. Un valor de -1 especifica que el método esperará hasta que la tarea se complete sin tiempo de espera. Otros valores de tiempo de espera válidos oscilan entre 0 y 4 000 000 milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>         |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>      | El *parámetro timeout* no es válido.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>     |



 

## <a name="remarks"></a>Comentarios

El **método WaitForCompletion** coloca el subproceso de ejecución actual en modo de suspensión hasta que se devuelve. No se recomienda especificar una espera infinita (tiempo de espera = -1) a menos que sea absolutamente crítico que la tarea se complete en cualquier circunstancia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMTask se define como \_ ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

