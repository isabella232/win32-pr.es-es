---
description: SetupScanFileQueue envía la notificación SPFILENOTIFY QUEUESCAN a una rutina de devolución de llamada para cada nodo de la subcola de copia \_ de la cola de archivos. Esto solo ocurre si se llamó a la función SetupScanFileQueue especificando la marca SPQ \_ SCAN \_ USE \_ CALLBACK.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: SPFILENOTIFY_QUEUESCAN mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab9c680ff2aaa3056ab74db741a34bb9f0379ec7123821b1de4c20200997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664855"
---
# <a name="spfilenotify_queuescan-message"></a>Mensaje DE SPFILENOTIFY \_ QUEUESCAN

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) envía la notificación **SPFILENOTIFY \_ QUEUESCAN** a una rutina de devolución de llamada para cada nodo de la subcola de copia de la cola de archivos. Esto solo ocurre si se llamó a **la función SetupScanFileQueue** especificando la marca SPQ \_ SCAN USE \_ \_ CALLBACK.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Cadena terminada en NULL que especifica la información de ruta de acceso de destino para el archivo en cola en el nodo actual.

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo del nodo actual de la cola está en uso, *Param2* toma el valor SPQ \_ DELAYED \_ COPY. Si el archivo no está en uso, el valor es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Si la rutina de devolución de llamada devuelve NO \_ ERROR, el examen de cola continúa. Si la rutina devuelve cualquier otro código de error, el examen de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve **FALSE.**

> [!Note]  
> La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

