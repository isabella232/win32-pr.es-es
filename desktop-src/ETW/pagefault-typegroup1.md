---
description: 'PageFault_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de error de página. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106413"
---
# <a name="pagefault_typegroup1-class"></a>Clase PageFault \_ TypeGroup1

Esta clase es la clase de tipo de evento para los eventos de error de página.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Miembros

La **clase PageFault \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase PageFault \_ TypeGroup1** tiene estas propiedades.

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Puntero a la instrucción actual que se ejecuta.

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección virtual de la página que produjo el error de la página.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Un error de página se produce cuando una página buscada en la memoria caché no se encuentra allí y se debe recuperar de otra parte de la memoria (un error temporal) o del disco (un error físico).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




