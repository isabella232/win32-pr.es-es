---
title: Estructura WMDMDATETIME
description: La estructura WMDMDATETIME contiene una fecha y hora del día.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estructura WMDMDATETIME windows Media Administrador de dispositivos
- Puntero de estructura PWMDMDATETIME windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9648b4c2d1272dcf00d45277119b51f438dba23d9eaf5e7810451fb693e8cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004635"
---
# <a name="wmdmdatetime-structure"></a>Estructura WMDMDATETIME

La **estructura WMDMDATETIME** contiene una fecha y hora del día.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wYear**
</dt> <dd>

Palabra que contiene el año de cuatro dígitos.

</dd> <dt>

**wMonth**
</dt> <dd>

Palabra que contiene el mes (1-12).

</dd> <dt>

**wDay**
</dt> <dd>

Palabra que contiene el día del mes (1-31).

</dd> <dt>

**wHour**
</dt> <dd>

Palabra que contiene la hora (0-23).

</dd> <dt>

**wMinute**
</dt> <dd>

Palabra que contiene el minuto (0-59).

</dd> <dt>

**wSecond**
</dt> <dd>

Palabra que contiene la segunda (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMDSPStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





