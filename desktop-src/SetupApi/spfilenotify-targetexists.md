---
description: La notificación SPFILENOTIFY TARGETEXISTS se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la marca \_ SP \_ COPY NOOVERWRITE y ese archivo ya existe en el directorio de \_ destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51f845d7ccb41b330f6365eff269645d08e58597e7e6dd3e9acc7a7f0300c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664745"
---
# <a name="spfilenotify_targetexists-message"></a>Mensaje SPFILENOTIFY \_ TARGETEXISTS

La **notificación SPFILENOTIFY \_ TARGETEXISTS** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la marca SP \_ COPY NOOVERWRITE y ese archivo ya existe en el directorio de \_ destino. Se puede enviar a la rutina de devolución de llamada por sí sola o combinarse, mediante el operador OR, con las notificaciones [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) o [**SPFILENOTIFY \_ TARGETNEWER.**](spfilenotify-targetnewer.md)


```C++
SPFILENOTIFY_TARGETEXISTS
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

Este parámetro no se usa a menos que esta notificación se combine, mediante el operador OR, con la [**notificación SPFILENOTIFY \_ LANGMISMATCH.**](spfilenotify-langmismatch.md)

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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
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

 

 




