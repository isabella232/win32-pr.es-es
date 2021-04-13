---
description: La \_ notificación SPFILENOTIFY TARGETEXISTS se envía a la rutina de devolución de llamada si el archivo que se va a copiar se puso en cola con la \_ marca NOOVERWRITE de la copia Sp \_ y ese archivo ya existe en el directorio de destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Mensaje de SPFILENOTIFY_TARGETEXISTS (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423983"
---
# <a name="spfilenotify_targetexists-message"></a>SPFILENOTIFY \_ TARGETEXISTS

La notificación **SPFILENOTIFY \_ TARGETEXISTS** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se puso en cola con la \_ marca NOOVERWRITE de la copia Sp \_ y ese archivo ya existe en el directorio de destino. Se puede enviar a la rutina de devolución de llamada solo o combinarse mediante el operador OR, con las notificaciones de [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) y/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .


```C++
SPFILENOTIFY_TARGETEXISTS
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

Este parámetro no se usa a menos que se combine esta notificación, mediante el operador OR, con la notificación [**\_ LANGMISMATCH de SPFILENOTIFY**](spfilenotify-langmismatch.md) .

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

 

 




