---
description: La notificación de LANGMISMATCH de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un archivo de destino existente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Mensaje de SPFILENOTIFY_LANGMISMATCH (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669716"
---
# <a name="spfilenotify_langmismatch-message"></a>SPFILENOTIFY \_ LANGMISMATCH

La notificación de **\_ LANGMISMATCH de SPFILENOTIFY** se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un archivo de destino existente. Se puede enviar a la rutina de devolución de llamada solo o combinarse mediante el operador OR, con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifica los idiomas no coincidentes. Este miembro tiene el identificador de idioma del archivo de código fuente en la palabra baja y el identificador de idioma del archivo de destino existente en la palabra alta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                          | Descripción                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>  | Copie el archivo y sobrescriba el archivo existente.<br/>               |
| <dl> <dt>**ES**</dt> </dl> | Omitir la operación de copia. No sobrescriba el archivo existente.<br/> |



 

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

 

 




