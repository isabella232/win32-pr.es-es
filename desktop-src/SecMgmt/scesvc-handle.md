---
description: El tipo de datos de identificador de SCESVC \_ es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540974"
---
# <a name="scesvc_handle"></a>identificador de SCESVC \_

El tipo de datos de **\_ identificador de SCESVC** es un identificador opaco proporcionado por el conjunto de herramientas de configuración de seguridad. Lo usan los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) y [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento configuración de seguridad y la extensión del complemento.


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




