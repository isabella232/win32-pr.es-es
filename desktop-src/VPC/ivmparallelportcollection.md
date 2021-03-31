---
title: Interfaz IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Define la colección de puertos paralelos dentro de la máquina virtual. Para obtener un objeto IVMParallelPortCollection, use la propiedad ParallelPorts de IVMVirtualMachine.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Interfaz IVMParallelPortCollection Virtual PC
- Interfaz IVMParallelPortCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151076"
---
# <a name="ivmparallelportcollection-interface"></a>Interfaz IVMParallelPortCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de puertos paralelos dentro de la máquina virtual. Para obtener un objeto **IVMParallelPortCollection** , use la propiedad [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Miembros

La interfaz **IVMParallelPortCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPortCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMParallelPortCollection** tiene estas propiedades.



| Propiedad                                                           | Tipo de acceso          | Descripción                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmparallelportcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                 |
| [**Contabiliza**](ivmparallelportcollection-count.md)<br/>        | Solo lectura<br/> | Número de puertos paralelos de esta colección.<br/>                  |
| [**Elemento**](ivmparallelportcollection-item.md)<br/>          | Solo lectura<br/> | Objeto de puerto paralelo que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMVirtualMachine::P arallelPorts**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

