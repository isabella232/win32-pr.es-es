---
description: El tipo de datos de identificador de SCE \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Lo usan \_ las funciones PFSCE Query \_ info y PFSCE \_ set \_ info support para pasar información entre los datos adjuntos y la base de datos de seguridad.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154074"
---
# <a name="sce_handle"></a>identificador de SCE \_

El tipo de datos de **\_ identificador de SCE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Lo usan las funciones [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support para pasar información entre los datos adjuntos y la base de datos de seguridad.


```C++
typedef PVOID SCE_HANDLE;
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
</dt> <dt>

[**PFSCE \_ establecer \_ información**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

