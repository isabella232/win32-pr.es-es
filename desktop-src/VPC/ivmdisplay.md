---
title: Interfaz IVMDisplay (VPCCOMInterfaces.h)
description: Controla la configuración de visualización de una máquina virtual. La interfaz IVMDisplay de una máquina virtual se puede recuperar mediante la propiedad IVMVirtualMachine Display.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- IVMDisplay interface Virtual PC
- IVMDisplay interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6239747477cdddf0ecbcf3acac90e33e61c0f5f4c9dd327b80eb6a33cb113c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654145"
---
# <a name="ivmdisplay-interface"></a>Interfaz IVMDisplay

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controla la configuración de visualización de una máquina virtual. La **interfaz IVMDisplay** de una máquina virtual se puede recuperar mediante la [**propiedad IVMVirtualMachine::D isplay.**](ivmvirtualmachine-display.md)

## <a name="members"></a>Miembros

La **interfaz IVMDisplay** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDisplay también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMDisplay** tiene estos métodos.



| Método                                                       | Descripción                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.<br/>                       |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMDisplay** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso          | Descripción                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Solo lectura<br/> | Indica si el invitado permite cambios de resolución.<br/>                             |
| [**Alto**](ivmdisplay-height.md)<br/>       | Solo lectura<br/> | Alto de la pantalla de la máquina virtual, en píxeles.<br/>                            |
| [**Miniatura**](ivmdisplay-thumbnail.md)<br/> | Solo lectura<br/> | Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Solo lectura<br/> | El modo de vídeo actual (Texto, VGA, SVGA, y así sucesivamente).<br/>                               |
| [**Ancho**](ivmdisplay-width.md)<br/>         | Solo lectura<br/> | Ancho de la pantalla de la máquina virtual, en píxeles.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay se define como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

