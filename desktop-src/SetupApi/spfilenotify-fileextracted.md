---
description: La notificación de FILEEXTRACTED de SPFILENOTIFY \_ se envía a una rutina de devolución de llamada de SetupIterateCabinet para indicar que un archivo se ha extraído del contenedor o que se ha producido un error en la extracción y se ha cancelado el procesamiento del archivo. cab.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Mensaje de SPFILENOTIFY_FILEEXTRACTED (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669717"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ FILEEXTRACTED

La notificación de **\_ FILEEXTRACTED de SPFILENOTIFY** se envía a una rutina de devolución de llamada de [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que un archivo se ha extraído del contenedor o que se ha producido un error en la extracción y se ha cancelado el procesamiento del archivo. cab.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre la ruta de acceso del archivo extraído. El miembro **SourceFile** de la estructura **FILEPATHS** contiene la ruta de acceso de origen completa del archivo. cab. El miembro **TargetFile** proporciona la ruta de acceso de destino completa del archivo que se va a instalar en el sistema.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada del archivo. cab debe devolver uno de los siguientes valores.



| Código devuelto                                                                               | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SIN \_ errores**</dt> </dl>  | No se encontró ningún error y continúe procesando el archivo. cab.<br/>                                                                                                                                |
| <dl> <dt>**ERROR \_ XXX**</dt> </dl> | Se produjo un error del tipo especificado. [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá cero. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error especificado.<br/> |



 

> [!Note]  
> No se ha proporcionado ninguna rutina de devolución de llamada de archivador predeterminada con la API de instalación. La aplicación de instalación debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

