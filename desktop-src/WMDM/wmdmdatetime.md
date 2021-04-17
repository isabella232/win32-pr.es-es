---
title: Estructura WMDMDATETIME
description: La estructura WMDMDATETIME contiene una fecha y hora del día.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estructura WMDMDATETIME Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMDATETIME Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698558"
---
# <a name="wmdmdatetime-structure"></a>Estructura WMDMDATETIME

La estructura **WMDMDATETIME** contiene una fecha y hora del día.

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

Palabra que contiene el segundo (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMDSPStorage:: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage:: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





