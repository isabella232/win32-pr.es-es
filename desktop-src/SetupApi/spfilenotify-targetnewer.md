---
description: La notificación SPFILENOTIFY TARGETNEWER se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con las marcas SP COPY NEWER o SP COPY FORCE NEWER especificadas y ya existe una versión más reciente del archivo en el directorio de \_ \_ \_ \_ \_ \_ destino.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: SPFILENOTIFY_TARGETNEWER mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a0c2a1aff8c42ea95c489a7fcc87e40221ca0405b3048d43e3de718f5f3b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964075"
---
# <a name="spfilenotify_targetnewer-message"></a>SPFILENOTIFY \_ TARGETNEWER message

La notificación **SPFILENOTIFY \_ TARGETNEWER** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con las marcas SP COPY NEWER o SP COPY FORCE NEWER especificadas y ya existe una versión más reciente del archivo en el directorio de \_ \_ \_ \_ \_ destino. Se puede enviar solo a la rutina de devolución de llamada o ARed junto con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) o [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Este parámetro no se usa a menos que esta notificación se combine, mediante el operador OR, [**con SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                          | Descripción                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | Sobrescriba el archivo en el directorio de destino.<br/> |
| <dl> <dt>**Falso**</dt> </dl> | Omita la operación de copia actual.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




