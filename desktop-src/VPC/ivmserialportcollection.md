---
title: Interfaz IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Define la colección de puertos serie dentro de la máquina virtual. Para obtener un objeto IVMSerialPortCollection, use la propiedad SerialPorts de IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Interfaz IVMSerialPortCollection Virtual PC
- Interfaz IVMSerialPortCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802455"
---
# <a name="ivmserialportcollection-interface"></a>Interfaz IVMSerialPortCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la colección de puertos serie dentro de la máquina virtual. Para obtener un objeto **IVMSerialPortCollection** , use la propiedad [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Miembros

La interfaz **IVMSerialPortCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPortCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMSerialPortCollection** tiene estas propiedades.



| Propiedad                                                         | Tipo de acceso          | Descripción                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_NewEnum**](ivmserialportcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                               |
| [**Contabiliza**](ivmserialportcollection-count.md)<br/>        | Solo lectura<br/> | Número de puertos serie de esta colección.<br/>                  |
| [**Elemento**](ivmserialportcollection-item.md)<br/>          | Solo lectura<br/> | Objeto de puerto serie que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection se define como dd3c6175-1F04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

