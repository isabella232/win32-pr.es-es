---
title: Interfaz IVMKeyboard (VPCCOMInterfaces. h)
description: Controla el dispositivo de teclado dentro de una máquina virtual. El IVMKeyboard de una máquina virtual se puede recuperar mediante la propiedad de teclado IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Interfaz IVMKeyboard Virtual PC
- Interfaz IVMKeyboard Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696042"
---
# <a name="ivmkeyboard-interface"></a>Interfaz IVMKeyboard

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla el dispositivo de teclado dentro de una máquina virtual. El **IVMKeyboard** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .

## <a name="members"></a>Miembros

La interfaz **IVMKeyboard** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMKeyboard** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMKeyboard** tiene estos métodos.



| Método                                                       | Descripción                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**IsPressed**](ivmkeyboard-ispressed.md)                   | Determina si la tecla especificada está presionada.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula que se presiona una tecla y luego se libera.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula que se presiona una tecla.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula una clave que se va a liberar.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula una serie de claves ASCII que se escriben en el invitado.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula una lista delimitada por comas de las claves que se escriben en el invitado.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMKeyboard** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso           | Descripción                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lectura/escritura<br/> | Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.<br/> |



 

## <a name="remarks"></a>Observaciones

Las claves se pueden escribir en la máquina virtual de varias maneras. Para escribir una secuencia ASCII normal de caracteres, utilice el método [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) . Si se requiere una mayor flexibilidad, **IVMKeyboard** tiene varios métodos que están diseñados para usarse con los códigos de tecla de la lista siguiente. El método [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) puede aceptar una cadena delimitada por comas de códigos de tecla, que se presionarán y liberarán, en orden, dentro de la máquina virtual. Además de estos códigos de tecla, se pueden usar las palabras clave hacia arriba y hacia abajo para forzar que una clave se presione solamente o se libere. Las palabras clave UP y DOWN solo se aplican al código de tecla que sigue directamente a la palabra clave.

Para evitar que varios scripts, aplicaciones o usuarios intenten acceder simultáneamente al mismo dispositivo de teclado, establezca la propiedad [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) en **true**. Si un proceso adquiere acceso exclusivo, cualquier intento por parte de otros procesos para enviar entradas al dispositivo de teclado se omitirá hasta que se libere el acceso exclusivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de Windows Virtual PC](virtual-pc-interfaces.md)
</dt> <dt>

[Secuencias de claves](key-sequences.md)
</dt> </dl>

 

