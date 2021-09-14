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
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245295"
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



## <a name="members"></a>Members

<dl> <dt>

**szColumnName**
</dt> <dd>

Nombre que se puede mostrar de una columna específica. Si el nombre es demasiado largo, no será completamente visible en la configuración Visor de eventos predeterminada.

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



 

 




