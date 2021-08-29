---
description: SetupInstallFileEx o SetupCommitFileQueue envían la notificación SPFILENOTIFY FILEOPDELAYED a una rutina de devolución de llamada cuando se retrasó una operación de archivo porque el archivo estaba \_ en uso. La operación se procesará la próxima vez que se reinicie el sistema.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: SPFILENOTIFY_FILEOPDELAYED mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c3034e7e3114bb3c55db48850cbe276c66702fc44cd67e54f0f1b47c93a2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665105"
---
# <a name="spfilenotify_fileopdelayed-message"></a>SPFILENOTIFY \_ FILEOPDELAYED message

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envían la notificación **SPFILENOTIFY \_ FILEOPDELAYED** a una rutina de devolución de llamada cuando se retrasó una operación de archivo porque el archivo estaba en uso. La operación se procesará la próxima vez que se reinicie el sistema.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

Si la operación retrasada es una operación de copia de archivos, la [**estructura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.



| Miembro FILEPATHS | Valor                                |
|------------------|--------------------------------------|
| **Win32Error**   | NO \_ ERROR                            |
| **Marcas**        | FILEOP \_ COPY                         |
| **Origen**       | Ruta de acceso completa del archivo temporal.     |
| **Target**       | Ruta de acceso completa del archivo de destino real. |



 

Este archivo temporal se copiará en el directorio de destino cuando se reinicie el sistema. Las funciones de instalación generan automáticamente una ruta de acceso para el archivo temporal.

Si la operación retrasada es una operación de eliminación de archivos, la [**estructura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.



| Miembro FILEPATHS | Valor                                |
|------------------|--------------------------------------|
| **Win32Error**   | NO \_ ERROR                            |
| **Marcas**        | FILEOP \_ DELETE                       |
| **Origen**       | NULL                                 |
| **Target**       | Ruta de acceso completa del archivo que se va a eliminar. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




