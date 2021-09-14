---
description: El tipo de datos \_ SCE HANDLE es un identificador opaco proporcionado por el conjunto de herramientas configuración de seguridad. PfSCE QUERY INFO y PFSCE SET INFO admiten funciones para pasar información entre los datos adjuntos y la \_ base de datos de \_ \_ \_ seguridad.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071119"
---
# <a name="sce_handle"></a>IDENTIFICADOR \_ de SCE

El **tipo de datos \_ SCE HANDLE** es un identificador opaco proporcionado por el conjunto de herramientas configuración de seguridad. PfSCE [**\_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) admiten funciones para pasar información entre los datos adjuntos y la base de datos de seguridad.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE CONSULTA \_ PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

