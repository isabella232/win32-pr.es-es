---
title: Método OnMediaEject de IVMFstonepyDriveEvents (VPCCOMInterfaces.h)
description: Recibe la notificación de que los medios se han expulsado de la unidad. | Método OnMediaEject de IVMFstonepyDriveEvents (VPCCOMInterfaces.h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- OnMediaEject, método Virtual PC
- Método OnMediaEject virtual PC , interfaz IVMFstonepyDriveEvents
- IVMFstonepyDriveEvents interface Virtual PC , Método OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e624dcbf028caf58a2f50109789e5f89cd34d1d70c4679333b8b742c3b071ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653605"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>IVMFstonepyDriveEvents::OnMediaEject (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que los medios se han expulsado de la unidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mediaPath* \[ En\]
</dt> <dd>

La letra de unidad de host, o ruta de acceso, a la imagen de disquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando se expulsa un medio (una imagen de disquete o un disquete en una unidad host). El programa cliente debe implementar este método de interfaz para recibir una notificación del evento vmFstonepyDriveEvent OnMediaEject que se origina \_ en [**IVMFstonepyDrive.**](ivmfloppydrive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

