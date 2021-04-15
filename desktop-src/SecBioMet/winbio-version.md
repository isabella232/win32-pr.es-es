---
title: Estructura de WINBIO_VERSION (Winbio \_ Types. h)
description: Contiene el número de versión de software de un componente de proveedor de servicios biométricos.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- Plataforma de biometría de Windows API de WINBIO_VERSION Structure
- PWINBIO_VERSION de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493018"
---
# <a name="winbio_version-structure"></a>Estructura de la versión de WINBIO \_

La estructura de la **\_ versión WINBIO** contiene el número de versión de software de un componente de proveedor de servicios biométricos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MajorVersion**
</dt> <dd>

**DWORD** que contiene el número de versión principal.

</dd> <dt>

**MinorVersion**
</dt> <dd>

**DWORD** que contiene el número de versión secundaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**\_esquema BSP de WINBIO \_**](winbio-bsp-schema.md)
</dt> <dt>

[**esquema de la \_ unidad WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





