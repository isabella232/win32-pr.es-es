---
title: Método IVMFstonepyDriveEvents OnMediaInsert (VPCCOMInterfaces.h)
description: Recibe la notificación de que se han insertado medios en la unidad. | Método IVMFstonepyDriveEvents OnMediaInsert (VPCCOMInterfaces.h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Equipo virtual del método OnMediaInsert
- Método OnMediaInsert de PC virtual, interfaz IVMFstonepyDriveEvents
- IVMFstonepyDriveEvents interface Virtual PC , OnMediaInsert (método)
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30eb00222304168b30f6512b51f9d381fc4fbd61e7c5d254e0d53c3eb931a819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594784"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>IVMFstonepyDriveEvents::OnMediaInsert (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que se han insertado medios en la unidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mediaPath* \[ En\]
</dt> <dd>

La letra de unidad del host, o ruta de acceso, a la imagen de disquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Se llama a este método cuando se insertan medios (una imagen de disquete o un disquete en una unidad host). El programa cliente debe implementar este método de interfaz para recibir la notificación del evento vmFstonepyDriveEvent OnMediaInsert que se origina \_ en [**IVMFstonepyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFstonepyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFstonepyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

