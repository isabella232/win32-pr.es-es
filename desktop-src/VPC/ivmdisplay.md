---
title: Interfaz IVMDisplay (VPCCOMInterfaces. h)
description: Controla la configuración de pantalla de una máquina virtual. La interfaz IVMDisplay de una máquina virtual se puede recuperar mediante la propiedad IVMVirtualMachine display.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Interfaz IVMDisplay Virtual PC
- Interfaz IVMDisplay Virtual PC, descripción
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
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996771"
---
# <a name="ivmdisplay-interface"></a>Interfaz IVMDisplay

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla la configuración de pantalla de una máquina virtual. La interfaz **IVMDisplay** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine::D**](ivmvirtualmachine-display.md) Mostrar.

## <a name="members"></a>Miembros

La interfaz **IVMDisplay** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDisplay** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMDisplay** tiene estos métodos.



| Método                                                       | Descripción                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.<br/>                       |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMDisplay** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso          | Descripción                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Solo lectura<br/> | Indica si el invitado permite cambios de resolución.<br/>                             |
| [**Height**](ivmdisplay-height.md)<br/>       | Solo lectura<br/> | Alto de la pantalla de la máquina virtual, en píxeles.<br/>                            |
| [**Miniatura**](ivmdisplay-thumbnail.md)<br/> | Solo lectura<br/> | Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.<br/> |
| [**Modo**](ivmdisplay-videomode.md)<br/> | Solo lectura<br/> | El modo de vídeo actual (texto, VGA, SVGA, etc.).<br/>                               |
| [**Width**](ivmdisplay-width.md)<br/>         | Solo lectura<br/> | Ancho de la pantalla de la máquina virtual, en píxeles.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

