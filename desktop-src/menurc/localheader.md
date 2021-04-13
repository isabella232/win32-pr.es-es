---
title: Estructura LOCALHEADER
description: Contiene las coordenadas x e y de una zona activa asociada al cursor identificado por una estructura RESDIR. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menús de la estructura LOCALHEADER y otros recursos
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422408"
---
# <a name="localheader-structure"></a>Estructura LOCALHEADER

Contiene las coordenadas x e y de una zona activa asociada al cursor identificado por una estructura [**RESDIR**](resdir.md) . La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**xHotSpot**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Coordenada x de la zona activa del cursor, en píxeles.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Coordenada y de la zona activa del cursor, en píxeles.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **LOCALHEADER** es la primera de los datos que se escriben en el recurso de [ \_ cursor RT](/windows/desktop/menurc/resource-types) si una estructura [**RESDIR**](resdir.md) contiene información sobre un cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

