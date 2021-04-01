---
description: Describe los datos del objeto de receptor de pantalla incluidos en un resultado de notificación o notificación.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER estructura (Wfdsink. h)
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
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909426"
---
# <a name="wfd_display_sink_object_header-structure"></a>\_Estructura de \_ encabezado de objeto de receptor de visualización de \_ WFD \_

La estructura de encabezado de objeto del receptor de visualización de WFD describe los datos del objeto de receptor de pantalla incluidos en un resultado de notificación o notificación. **\_ \_ \_ \_**

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

Tipo del objeto de receptor de pantalla. Puede usar el identificador predeterminado de **\_ tipo de \_ \_ objeto de \_ \_ receptor de visualización de WFD** , que se define como el valor 1.

</dd> <dt>

**Revisión**
</dt> <dd>

Versión de revisión del objeto de receptor de pantalla. Puede usar el identificador de la **revisión del objeto del receptor de visualización de la \_ \_ \_ \_ \_ versión \_ 1** del identificador, que se define como el valor 1.

</dd> <dt>

**Duración**
</dt> <dd>

La longitud de los datos en el resultado de notificación o notificación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




