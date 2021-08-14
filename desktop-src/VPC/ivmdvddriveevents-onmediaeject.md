---
title: Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces.h)
description: Recibe la notificación de que los medios se han expulsado de la unidad. | Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces.h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- OnMediaEject, método Virtual PC
- Método OnMediaEject De PC virtual, interfaz IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC , Método OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2fbf9ffe589597e1baab7c0b503cf94384cfa540749cfe49e083286f743370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753756"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>IVMDVDDriveEvents::OnMediaEject (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

La letra de unidad del host, o ruta de acceso, a la imagen ISO.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando se expulsa un medio (una imagen ISO o un disco en una unidad host). El programa cliente debe implementar este método de interfaz para recibir la notificación del evento vmDVDDriveEvent OnEject que se \_ origina en [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

