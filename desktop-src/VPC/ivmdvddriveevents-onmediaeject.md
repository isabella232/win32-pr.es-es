---
title: Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha expulsado el medio de la unidad. | Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Método OnMediaEject Virtual PC
- Método OnMediaEject Virtual PC, interfaz IVMDVDDriveEvents
- Interfaz IVMDVDDriveEvents Virtual PC, método OnMediaEject
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
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914353"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>IVMDVDDriveEvents:: OnMediaEject (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recibe la notificación de que se ha expulsado el medio de la unidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mediaPath* \[ de\]
</dt> <dd>

La letra de la unidad del host, o ruta de acceso, a la imagen ISO.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cuando se expulsa un medio (una imagen ISO o un disco de una unidad de host). El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento VmDVDDriveEvent EJECT que se origina desde [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

