---
description: SetupScanFileQueue envía la notificación SPFILENOTIFY QUEUESCAN EX a una rutina de devolución de llamada para cada nodo de la subcola de copia \_ de la cola de \_ archivos.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: SPFILENOTIFY_QUEUESCAN_EX mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992595"
---
# <a name="spfilenotify_queuescan_ex-message"></a>SpFILENOTIFY \_ QUEUESCAN \_ EX message

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) envía la notificación **SPFILENOTIFY \_ QUEUESCAN \_ EX** a una rutina de devolución de llamada para cada nodo de la subcola de copia de la cola de archivos. Esto solo ocurre si se llamó a **la función SetupScanFileQueue** especificando la marca SPQ \_ SCAN USE \_ \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) El **miembro** Target es el nombre de archivo del archivo de destino en el sistema. El **miembro Source** es la ruta de acceso esperada del archivo de origen. El **miembro Win32Error** es el error de firma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Si la rutina de devolución de llamada devuelve NO \_ ERROR, el examen de cola continúa. Si la rutina devuelve cualquier otro código de error, el examen de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve FALSE.

> [!Note]  
> La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

