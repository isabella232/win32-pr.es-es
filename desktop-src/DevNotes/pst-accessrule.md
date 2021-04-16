---
description: Describe una regla para el acceso a los elementos almacenados en el almacenamiento protegido.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650025"
---
# <a name="pst_accessrule-structure"></a>\_Estructura ACCESSRULE de PST

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Describe una regla para el acceso a los elementos almacenados en el almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

Los modos de acceso a los que pertenece un conjunto especificado de cláusulas de acceso.



| Value                                                                                                                                                                                                         | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Archivo pst \_ LEER**</dt> <dt>0x0001</dt> </dl>    | Modo de acceso de lectura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Archivo pst \_ ESCRIBIR**</dt> <dt>0x0002</dt> </dl> | Modo de acceso de escritura.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

El número de estructuras de la matriz **rgClauses** .

</dd> <dt>

**rgClauses**
</dt> <dd>

Puntero a una matriz de estructuras [**\_ ACCESSCLAUSE de PST**](pst-accessclause.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PST \_ ACCESSCLAUSE**](pst-accessclause.md)
</dt> <dt>

[**PST \_ ACCESSRULESET**](pst-accessruleset.md)
</dt> </dl>

 

 
