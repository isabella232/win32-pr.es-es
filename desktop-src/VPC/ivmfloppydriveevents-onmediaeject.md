---
title: Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha expulsado el medio de la unidad. | Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- Método OnMediaEject Virtual PC
- Método OnMediaEject Virtual PC, interfaz IVMFloppyDriveEvents
- Interfaz IVMFloppyDriveEvents Virtual PC, método OnMediaEject
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
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914673"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>IVMFloppyDriveEvents:: OnMediaEject (método)

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

La letra de unidad del host, o ruta de acceso, a la imagen de disquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cuando se expulsa un medio (una imagen de disquete o un disquete en una unidad de host). El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmFloppyDriveEvent OnMediaEject que se origina desde [**IVMFloppyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

