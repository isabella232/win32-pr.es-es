---
description: Los tipos de datos para los métodos de almacenamiento protegido.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: PStore (tipos) (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649828"
---
# <a name="pstore-types"></a>PStore (tipos)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Los tipos de datos para los métodos de almacenamiento protegido.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST \_ ACCESSMODE**
</dt> <dd>

Define el modo de lectura o escritura de la regla de acceso.

</dd> <dt>

**PST \_ ACCESSCLAUSETYPE**
</dt> <dd>

Define el tipo de cláusula de la regla de acceso.

</dd> <dt>

**\_clave PST**
</dt> <dd>

Define la clave para el elemento almacenado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
