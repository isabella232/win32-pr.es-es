---
title: Interfaz IVMMouse (VPCCOMInterfaces.h)
description: Controla el dispositivo del mouse dentro de una máquina virtual.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- IVMMouse interface Virtual PC
- IVMMouse interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912365065b639f3c970390746c8e23ae1fc33648ecdf14278365290c503da26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998855"
---
# <a name="ivmmouse-interface"></a>Interfaz IVMMouse

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controla el dispositivo del mouse dentro de una máquina virtual (VM). La **IVMMouse** de una máquina virtual se puede recuperar mediante la [**propiedad IVMVirtualMachine::Mouse.**](ivmvirtualmachine-mouse.md) Las coordenadas del dispositivo del mouse se pueden representar en coordenadas absolutas o en coordenadas delta. Use la [**propiedad UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) para distinguir entre los dos métodos de representación de coordenadas. Tenga en cuenta que la recuperación de la posición actual del cursor y el uso de coordenadas absolutas solo se admiten si el sistema operativo invitado tiene instalados los componentes de integración.

## <a name="members"></a>Miembros

La **interfaz IVMMouse** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMMouse también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMMouse** tiene estos métodos.



| Método                                  | Descripción                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Hacer clic**](ivmmouse-click.md)         | Simula un clic del botón del mouse.<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | Recupera el estado actual (arriba o abajo) del botón del mouse especificado.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Establece el estado actual (arriba o abajo) del botón del mouse especificado.<br/>      |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMMouse** tiene estas propiedades.



| Propiedad                                                                         | Tipo de acceso           | Descripción                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**Horizontalposition**](ivmmouse-horizontalposition.md)<br/>             | Lectura/escritura<br/> | Coordenada x absoluta del mouse.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Solo escritura<br/> | Coordenada z del mouse (solo relativa).<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Lectura/escritura<br/> | Indica si las coordenadas del mouse representan coordenadas absolutas o relativas.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Lectura/escritura<br/> | Coordenada y absoluta del mouse.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse se define como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

