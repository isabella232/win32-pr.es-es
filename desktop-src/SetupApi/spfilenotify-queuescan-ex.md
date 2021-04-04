---
description: La \_ notificación SPFILENOTIFY QUEUESCAN \_ ex se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Mensaje de SPFILENOTIFY_QUEUESCAN_EX (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908809"
---
# <a name="spfilenotify_queuescan_ex-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ ex

La notificación **SPFILENOTIFY \_ QUEUESCAN \_ ex** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos. Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . El miembro de **destino** es el nombre de archivo del archivo de destino en el sistema. El miembro de **origen** es la ruta de acceso esperada del archivo de código fuente. El miembro **Win32Error** es el error de firma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa. Si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve false.

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

 

