---
description: El tipo de datos SCESVC HANDLE es un identificador \_ opaco proporcionado por el conjunto de herramientas de configuración de seguridad.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (Scesvc.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071117"
---
# <a name="scesvc_handle"></a>IDENTIFICADOR \_ SCESVC

El **tipo de datos \_ SCESVC HANDLE** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Lo usan los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento Configuración de seguridad y la extensión del complemento.


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




