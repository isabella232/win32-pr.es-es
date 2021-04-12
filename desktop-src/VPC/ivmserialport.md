---
title: Interfaz IVMSerialPort (VPCCOMInterfaces. h)
description: Define un puerto serie dentro de una máquina virtual.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Interfaz IVMSerialPort Virtual PC
- Interfaz IVMSerialPort Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534780"
---
# <a name="ivmserialport-interface"></a>Interfaz IVMSerialPort

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define un puerto serie dentro de una máquina virtual. Esta interfaz permite configurar puertos serie dentro de una máquina virtual. Puede recuperar un objeto **IVMSerialPort** del objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Miembros

La interfaz **IVMSerialPort** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPort** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMSerialPort** tiene estos métodos.



| Método                                       | Descripción                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_id**](ivmserialport--id.md)            | Recupera el identificador interno del puerto serie.<br/> |
| [**Configuración**](ivmserialport-configure.md) | Configura el puerto serie.<br/>                           |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMSerialPort** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso          | Descripción                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Solo lectura<br/> | Indica si se debe abrir el puerto serie sin esperar a que se reciba un comando de módem.<br/> |
| [**Name**](ivmserialport-name.md)<br/>                             | Solo lectura<br/> | Nombre del puerto serie.<br/>                                                                           |
| [**Tipo**](ivmserialport-type.md)<br/>                             | Solo lectura<br/> | Tipo del puerto serie.<br/>                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



 

