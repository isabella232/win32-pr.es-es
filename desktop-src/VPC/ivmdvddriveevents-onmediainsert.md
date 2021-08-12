---
title: Método OnMediaInsert de IVMDVDDriveEvents (VPCCOMInterfaces.h)
description: Recibe una notificación que informa de que se ha insertado un medio en la unidad. | Método OnMediaInsert de IVMDVDDriveEvents (VPCCOMInterfaces.h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Equipo virtual del método OnMediaInsert
- Método OnMediaInsert virtual PC , interfaz IVMDVDDriveEvents
- Interfaz IVMDVDDriveEvents Pc virtual, método OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b19beabfcc4cab182af850d27d3d45ea565b266e8bcaa8fa2488aa145f43fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595739"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>IVMDVDDriveEvents::OnMediaInsert (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe una notificación que informa de que se ha insertado un medio en la unidad.

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

La letra de unidad de host, o ruta de acceso, a la imagen ISO.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Se llama a este método cuando se insertan medios (una imagen ISO o un disco en una unidad host). El programa cliente debe implementar este método de interfaz para recibir una notificación del evento vmDVDDriveEvent OnInsert que se origina \_ en [**IVMDVDDrive.**](ivmdvddrive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

