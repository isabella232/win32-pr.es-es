---
description: El \_ tipo de datos de contexto de enumeración de SCE \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. La función información de consulta PFSCE la usa \_ \_ para navegar por la base de datos de seguridad.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360222"
---
# <a name="sce_enumeration_context"></a>\_contexto de enumeración de SCE \_

El tipo de datos de **\_ \_ contexto de enumeración de SCE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. La función [**\_ \_ información de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) la usa para navegar por la base de datos de seguridad.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información de consulta de PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

