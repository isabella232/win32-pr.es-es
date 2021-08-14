---
title: WINBIO_VERSION estructura (Winbio \_ types.h)
description: Contiene el número de versión de software de un componente de proveedor de servicios biométricos.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION estructura Windows API de Marco biométrico
- PWINBIO_VERSION puntero de estructura Windows API de Marco biométrico
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
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909120"
---
# <a name="winbio_version-structure"></a>Estructura DE \_ VERSIÓN DE WINBIO

La **estructura VERSIÓN \_ DE WINBIO** contiene el número de versión de software de un componente de proveedor de servicios biométricos.

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

DWORD **que** contiene el número de versión principal.

</dd> <dt>

**MinorVersion**
</dt> <dd>

DWORD **que** contiene el número de versión secundaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**ESQUEMA \_ BSP DE \_ WINBIO**](winbio-bsp-schema.md)
</dt> <dt>

[**ESQUEMA DE \_ UNIDAD \_ WINBIO**](winbio-unit-schema.md)
</dt> </dl>

 

 





