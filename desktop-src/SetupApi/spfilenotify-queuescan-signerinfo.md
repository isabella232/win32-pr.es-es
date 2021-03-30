---
description: La \_ notificación SPFILENOTIFY QUEUESCAN \_ SIGNERINFO se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Mensaje de SPFILENOTIFY_QUEUESCAN_SIGNERINFO (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002326"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO

La notificación **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos. Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ callback \_ SIGNERINFO. Disponible a partir de Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura de [**\_ SIGNERINFO de FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) . El miembro de **destino** es el nombre de archivo del archivo de destino en el sistema. El miembro de **origen** es la ruta de acceso esperada del archivo de código fuente. El miembro **Win32Error** es el error de firma. Se devuelve la información de la firma si la rutina de devolución de llamada devuelve **Win32Error**= = no hay ningún \_ error. El miembro **DigitalSigner** es el firmante digital. El miembro **version** es la versión. **CatalogFile** es el archivo de catálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa y devuelve si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve **false**.

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

 

