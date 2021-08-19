---
title: Estructura LOCALHEADER
description: Contiene las coordenadas x e y de un punto de acceso asociado al cursor identificado por una estructura RESDIR. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menús de estructura LOCALHEADER y otros recursos
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ec46b802b847b73c99cc81939531d8f9ec1a6a2e0addb4c928d5610ac5b80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870323"
---
# <a name="localheader-structure"></a>Estructura LOCALHEADER

Contiene las coordenadas x e y de un punto de acceso asociado al cursor identificado por una [**estructura RESDIR.**](resdir.md) La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

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

Tipo: **WORD**

</dd> <dd>

Coordenada x del punto de acceso directo del cursor, en píxeles.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Coordenada y del punto de acceso directo del cursor, en píxeles.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura LOCALHEADER** son los primeros datos escritos en el recurso [RT \_ CURSOR](/windows/desktop/menurc/resource-types) si una [**estructura RESDIR**](resdir.md) contiene información sobre un cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

