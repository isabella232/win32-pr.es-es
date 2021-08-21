---
description: El tipo de datos SCE HANDLE es un identificador \_ opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Las funciones de compatibilidad de PFSCE QUERY INFO y PFSCE SET INFO lo usan para pasar información entre los datos adjuntos y la \_ base de datos de \_ \_ \_ seguridad.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e9023cb03a906b154c8bedd70370c5e3c3d9a4679f71504102e222ae0442d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893536"
---
# <a name="sce_handle"></a>Identificador \_ de SCE

El **tipo de datos \_ SCE HANDLE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Las funciones de compatibilidad [**DE PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) lo usan para pasar información entre los datos adjuntos y la base de datos de seguridad.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE CONSULTA \_ PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**INFORMACIÓN DEL CONJUNTO DE PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

