---
description: '\_SetupInstallFileEx o SetupCommitFileQueue envía la notificación SPFILENOTIFY FILEOPDELAYED a una rutina de devolución de llamada cuando se retrasa una operación de archivo porque el archivo estaba en uso. La operación se procesará la próxima vez que se reinicie el sistema.'
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Mensaje de SPFILENOTIFY_FILEOPDELAYED (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908810"
---
# <a name="spfilenotify_fileopdelayed-message"></a>SPFILENOTIFY \_ FILEOPDELAYED

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envía la notificación **SPFILENOTIFY \_ FILEOPDELAYED** a una rutina de devolución de llamada cuando se retrasa una operación de archivo porque el archivo estaba en uso. La operación se procesará la próxima vez que se reinicie el sistema.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

Si la operación retrasada es una operación de copia de archivos, la estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.



| Miembro FILEPATHS | Value                                |
|------------------|--------------------------------------|
| **Win32Error**   | SIN \_ errores                            |
| **Marcas**        | copia de FILEOP \_                         |
| **Origen**       | Ruta de acceso completa del archivo temporal.     |
| **Target**       | Ruta de acceso completa del archivo de destino real. |



 

Este archivo temporal se copiará en el directorio de destino cuando se reinicie el sistema. Las funciones de configuración generan automáticamente una ruta de acceso para el archivo temporal.

Si la operación retrasada es una operación de eliminación de archivo, la estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.



| Miembro FILEPATHS | Value                                |
|------------------|--------------------------------------|
| **Win32Error**   | SIN \_ errores                            |
| **Marcas**        | FILEOP \_ eliminar                       |
| **Origen**       | NULL                                 |
| **Target**       | Ruta de acceso completa del archivo que se va a eliminar. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

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

 

 




