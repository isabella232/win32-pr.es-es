---
description: La notificación de TARGETNEWER de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la copia de SP \_ \_ más reciente o se \_ \_ \_ han especificado las marcas más recientes en el directorio de destino.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Mensaje de SPFILENOTIFY_TARGETNEWER (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667657"
---
# <a name="spfilenotify_targetnewer-message"></a>SPFILENOTIFY \_ TARGETNEWER

La notificación de **\_ TARGETNEWER de SPFILENOTIFY** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la copia de SP \_ \_ más reciente o se \_ \_ \_ han especificado las marcas más recientes en el directorio de destino. Se puede enviar a la rutina de devolución de llamada solo o a ORed junto con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) o [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Este parámetro no se usa a menos que se combine esta notificación, mediante el operador OR, con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                          | Descripción                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>  | Sobrescriba el archivo en el directorio de destino.<br/> |
| <dl> <dt>**ES**</dt> </dl> | Omitir la operación de copia actual.<br/>            |



 

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

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




