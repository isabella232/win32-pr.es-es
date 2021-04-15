---
title: Propiedad de error IVMTask (VPCCOMInterfaces. h)
description: Recupera el error registrado para esta tarea.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propiedad error Virtual PC
- Propiedad error Virtual PC, interfaz IVMTask
- Interfaz IVMTask Virtual PC, propiedad error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695960"
---
# <a name="ivmtaskerror-property"></a>IVMTask:: error (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el error registrado para esta tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>Valor de propiedad

Error registrado.

## <a name="error-codes"></a>Códigos de error

Las instancias de [**IVMTask**](ivmtask.md) devueltas por otras interfaces pueden devolver valores adicionales. Para obtener más información, consulte la documentación de los métodos que devuelven una instancia de **IVMTask** .



| Nombre o valor                                                                                                                                                                        | Significado                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                           | La operación se realizó correctamente.<br/>                              |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                             | El valor del parámetro es **null**.<br/>                           |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                     | Se produjo un error inesperado.<br/>                          |
| <dl> <dt>Máquina virtual \_ E \_ VMVIRTUALPC \_ \_ versión anterior</dt> <dt>0xA0040952</dt> </dl>     | Tanto Virtual PC 2007 como Windows Virtual PC están instalados.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ otro \_ \_ software de virtualización</dt> <dt>0xA0040953</dt> </dl> | Se instala otro software de virtualización.<br/>                |



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

 

