---
description: Este tema se aplica a Windows XP Service Pack 2 o posterior. La \_ estructura de conexión KSTOPOLOGY describe una conexión de nodo dentro de un filtro de streaming de kernel (KS). Un nodo puede estar conectado a otro nodo dentro del filtro o a un PIN en el filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION estructura (KS. h)
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
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690656"
---
# <a name="kstopology_connection-structure"></a>Estructura de conexión de KSTOPOLOGY \_

Este tema se aplica a Windows XP Service Pack 2 o posterior.

La estructura de **\_ conexión KSTOPOLOGY** describe una conexión de nodo dentro de un filtro de streaming de kernel (KS). Un nodo puede estar conectado a otro nodo dentro del filtro o a un PIN en el filtro.

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

Índice del nodo ascendente de la conexión. Si la conexión ascendente es un PIN, en lugar de un nodo, el valor es el \_ nodo KSFILTER.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Si el valor del campo **FromNode** es KSFILTER \_ nodo, este campo especifica el índice del PIN ascendente. De lo contrario, se omite este campo.

</dd> <dt>

**ToNode**
</dt> <dd>

Índice del nodo de nivel inferior en la conexión. Si la conexión de bajada es un PIN, en lugar de un nodo, el valor es el \_ nodo KSFILTER.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Si el valor del campo **ToNode** es KSFILTER \_ nodo, este campo especifica el índice del código PIN de nivel inferior. De lo contrario, se omite este campo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo:: get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




