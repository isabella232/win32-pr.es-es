---
title: Interfaz IVMKeyboard (VPCCOMInterfaces.h)
description: Controla el dispositivo de teclado dentro de una máquina virtual. El IVMKeyboard de una máquina virtual se puede recuperar mediante la propiedad IVMVirtualMachine Keyboard.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- IVMKeyboard interface Virtual PC
- IVMKeyboard interface Virtual PC , descrito
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
ms.openlocfilehash: 7284c4e2bb164cd53c8a34357c881ed096f342ae2c2230422985fac4c1fdae9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344803"
---
# <a name="ivmkeyboard-interface"></a>IVMKeyboard (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controla el dispositivo de teclado dentro de una máquina virtual. El **IVMKeyboard** de una máquina virtual se puede recuperar mediante la [**propiedad IVMVirtualMachine::Keyboard.**](ivmvirtualmachine-keyboard.md)

## <a name="members"></a>Miembros

La **interfaz IVMKeyboard** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMKeyboard** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMKeyboard** tiene estos métodos.



| Método                                                       | Descripción                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**IsPressed**](ivmkeyboard-ispressed.md)                   | Determina si la clave especificada está abajo.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula una tecla presionada y luego liberada.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula una tecla presionada.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula una clave que se va a liberar.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula una serie de claves ASCII que se escriben en el invitado.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula una lista delimitada por comas de claves que se escriben en el invitado.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMKeyboard** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso           | Descripción                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lectura/escritura<br/> | Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.<br/> |



 

## <a name="remarks"></a>Comentarios

Las claves se pueden escribir en la máquina virtual de varias maneras. Para escribir una secuencia ASCII normal de caracteres, use el [**método TypeAsciiText.**](ivmkeyboard-typeasciitext.md) Si se requiere mayor flexibilidad, **IVMKeyboard** tiene varios métodos diseñados para usarse con los códigos de clave de la lista siguiente. El [**método TypeKeySequence**](ivmkeyboard-typekeysequence.md) puede aceptar una cadena delimitada por comas de códigos de clave, que se presionarán y liberarán, en orden, dentro de la máquina virtual. Además de estos códigos de clave, las palabras clave UP y DOWN se pueden usar para forzar que una tecla solo se presione o solo se liberará. Las palabras clave UP y DOWN solo se aplican al código de clave directamente después de la palabra clave .

Para evitar que varios scripts, aplicaciones o usuarios intenten acceder simultáneamente al mismo dispositivo de teclado, establezca la propiedad [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) en **TRUE.** Si un proceso adquiere acceso exclusivo, los intentos de otros procesos de enviar entradas al dispositivo de teclado se omitirán hasta que se haya liberado el acceso exclusivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMKeyboard se define como \_ 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Virtual PC Interfaces](virtual-pc-interfaces.md)
</dt> <dt>

[Secuencias de claves](key-sequences.md)
</dt> </dl>

 

