---
description: Contiene información sobre la cláusula de acceso para el almacenamiento protegido.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670511"
---
# <a name="pst_accessclause-structure"></a>\_Estructura ACCESSCLAUSE de PST

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Contiene información sobre la cláusula de acceso para el almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**ClauseType**
</dt> <dd>

El tipo de datos al que apunta el miembro **pbClauseData** . Para obtener más información, vea [**PStore Types**](pstore-types.md).

</dd> <dt>

**cbClauseData**
</dt> <dd>

Tamaño de los datos a los que apunta el miembro **pbClauseData** .

</dd> <dt>

**pbClauseData**
</dt> <dd>

Puntero a los datos de la cláusula de acceso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PST \_ ACCESSRULE**](pst-accessrule.md)
</dt> </dl>

 

 
