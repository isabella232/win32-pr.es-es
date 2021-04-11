---
title: Propiedad IVMVirtualPC MaximumFloppyDrivesPerVM (VPCCOMInterfaces. h)
description: Recupera el número máximo de unidades de disquete por máquina virtual.
ms.assetid: f0dc351b-73de-4b6b-a953-5d5b683c4e31
keywords:
- Propiedad MaximumFloppyDrivesPerVM Virtual PC
- Propiedad MaximumFloppyDrivesPerVM Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad MaximumFloppyDrivesPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumFloppyDrivesPerVM
- IVMVirtualPC.get_MaximumFloppyDrivesPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc0d672affce5364e1658d5198681268109a1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150939"
---
# <a name="ivmvirtualpcmaximumfloppydrivespervm-property"></a>IVMVirtualPC:: MaximumFloppyDrivesPerVM (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número máximo de unidades de disquete por máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaximumFloppyDrivesPerVM(
  [out, retval] long *maxDrives
);
```



## <a name="property-value"></a>Valor de propiedad

Número máximo de unidades de disquete por máquina virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **null**.<br/>                                                           |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

