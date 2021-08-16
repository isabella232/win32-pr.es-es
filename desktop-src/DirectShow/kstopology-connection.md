---
description: Este tema se aplica a Windows XP Service Pack 2 o posterior. La estructura KSTOPOLOGY \_ CONNECTION describe una conexión de nodo dentro de un filtro de kernel-streaming (KS). Un nodo se puede conectar a otro nodo dentro del filtro o a un pin en el filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION estructura (Ks.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397249"
---
# <a name="kstopology_connection-structure"></a>Estructura DE CONEXIÓN KSTOPOLOGY \_

Este tema se aplica a Windows XP Service Pack 2 o posterior.

La **estructura KSTOPOLOGY \_ CONNECTION** describe una conexión de nodo dentro de un filtro de kernel-streaming (KS). Un nodo se puede conectar a otro nodo dentro del filtro o a un pin en el filtro.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FromNode**
</dt> <dd>

Índice del nodo ascendente en la conexión. Si la conexión ascendente es un pin, en lugar de un nodo, el valor es KSFILTER \_ NODE.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Si el valor del campo **FromNode** es KSFILTER NODE, este campo especifica el \_ índice del pin ascendente. De lo contrario, este campo se omite.

</dd> <dt>

**ToNode**
</dt> <dd>

Índice del nodo de bajada en la conexión. Si la conexión de bajada es un pin, en lugar de un nodo, el valor es KSFILTER \_ NODE.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Si el valor del **campo ToNode** es KSFILTER NODE, este campo especifica el índice del \_ pin de bajada. De lo contrario, este campo se omite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo::get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




