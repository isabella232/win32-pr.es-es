---
title: Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Recibe la notificación de que los medios se han insertado en la unidad. | Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Método OnMediaInsert Virtual PC
- Método OnMediaInsert Virtual PC, interfaz IVMDVDDriveEvents
- Interfaz IVMDVDDriveEvents Virtual PC, método OnMediaInsert
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
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003524"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>IVMDVDDriveEvents:: OnMediaInsert (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recibe la notificación de que los medios se han insertado en la unidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnMediaInsert(
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

Se llama a este método cuando se inserta un medio (una imagen ISO o un disco en una unidad de host). El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmDVDDriveEvent alinsert que se origina desde [**IVMDVDDrive**](ivmdvddrive.md).

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

 

