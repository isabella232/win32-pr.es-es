---
description: Esta clase es la clase de tipo de evento para los eventos de error de página. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911042"
---
# <a name="pagefault_transitionfault-class"></a>Errores \_ TransitionFault (clase)

Esta clase es la clase de tipo de evento para los eventos de error de página.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Miembros

La clase **errores \_ TransitionFault** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **errores \_ TransitionFault** tiene estas propiedades.

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Puntero a la instrucción actual que se está ejecutando.

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección virtual de la página que causó el error de página.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Errores \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




