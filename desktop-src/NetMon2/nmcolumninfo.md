---
description: La estructura NMCOLUMNINFO define una columna en el panel superior del Visor de eventos.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Estructura NMCOLUMNINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037125"
---
# <a name="nmcolumninfo-structure"></a>NMCOLUMNINFO (estructura)

La **estructura NMCOLUMNINFO** define una columna en el panel superior del Visor de eventos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szColumnName**
</dt> <dd>

Nombre que se puede mostrar de una columna específica. Si el nombre es demasiado largo, no estará completamente visible en la configuración Visor de eventos predeterminada.

</dd> <dt>

**VariantData**
</dt> <dd>

Datos insertados en la columna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




