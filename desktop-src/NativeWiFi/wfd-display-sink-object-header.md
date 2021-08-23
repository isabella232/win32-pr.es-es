---
description: Describe los datos del objeto receptor de visualización incluidos en un resultado de notificación o notificación.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER estructura (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: e4c9e4d83fbac1cccb2dbc0643acc707176be433dfca7854395a0f97c9c36435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800475"
---
# <a name="wfd_display_sink_object_header-structure"></a>ESTRUCTURA DE ENCABEZADO \_ DE OBJETO DE RECEPTOR DE VISUALIZACIÓN \_ \_ \_ DE WFD

La **estructura WFD \_ DISPLAY SINK \_ OBJECT \_ \_ HEADER** describe los datos del objeto receptor de visualización incluidos en un resultado de notificación o notificación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo del objeto receptor de visualización. Puede usar el identificador **WFD \_ DISPLAY SINK OBJECT TYPE \_ \_ \_ \_ DEFAULT,** que se define como el valor 1.

</dd> <dt>

**Revisión**
</dt> <dd>

Versión de revisión del objeto receptor de pantalla. Puede usar el identificador **WFD \_ DISPLAY SINK OBJECT REVISION VERSION \_ \_ \_ \_ \_ 1,** que se define como el valor 1.

</dd> <dt>

**Duración**
</dt> <dd>

Longitud de los datos en el resultado de la notificación o notificación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




