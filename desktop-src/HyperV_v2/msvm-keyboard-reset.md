---
description: 'Método reset de la Msvm_Keyboard clase : restablece el teclado virtual.'
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Método reset de la Msvm_Keyboard clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 14c3166ce57fab4693dec87d3d81a55f1f688aa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111713"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a>Método Reset de la clase Keyboard de Msvm \_

Restablece el teclado virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Un valor devuelto de cero indica que el resultado es correcto. Un valor devuelto de uno indica un error porque no se admite el método .

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1 solo \[ aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Teclado de \_ Msvm**](msvm-keyboard.md)
</dt> </dl>

 

 




