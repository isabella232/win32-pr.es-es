---
description: La notificación de QUEUESCAN de SPFILENOTIFY \_ se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos. Esto solo se produce si se llamó a la función SetupScanFileQueue especificando la marca SPQ \_ scan \_ use \_ callback.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Mensaje de SPFILENOTIFY_QUEUESCAN (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668174"
---
# <a name="spfilenotify_queuescan-message"></a>SPFILENOTIFY \_ QUEUESCAN

La notificación de **\_ QUEUESCAN de SPFILENOTIFY** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos. Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ callback.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Cadena terminada en null que especifica la información de la ruta de acceso de destino para el archivo en cola en el nodo actual.

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo del nodo actual de la cola está en uso, *parám2* toma el valor SPQ \_ copia retrasada \_ . Si el archivo no está en uso, el valor es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa. Si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve **false**.

> [!Note]  
> La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

