---
title: Método IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Método WaitForCompletion Virtual PC
- Método WaitForCompletion Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, método WaitForCompletion
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
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695988"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask:: WaitForCompletion (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tiempo de espera* \[ de\]
</dt> <dd>

Tiempo, en milisegundos, que este método esperará a la finalización de la tarea antes de devolver el control al autor de la llamada. Un valor de-1 especifica que el método esperará hasta que se complete la tarea sin que se agote el tiempo de espera. Otros valores de tiempo de espera válidos oscilan entre 0 y 4 millones milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | El parámetro *timeout* no es válido.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>     |



 

## <a name="remarks"></a>Observaciones

El método **WaitForCompletion** coloca el subproceso de ejecución actual en modo de suspensión hasta que lo devuelve. No se recomienda especificar una espera infinita (timeout =-1) a menos que sea absolutamente crítico que la tarea se complete en cualquier circunstancia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

