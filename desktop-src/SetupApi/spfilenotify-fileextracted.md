---
description: SetupIterateCabinet envía la notificación SPFILENOTIFY FILEEXTRACTED a una rutina de devolución de llamada para indicar que se extrajo un archivo del gabinete o que se ha cancelado una extracción y se ha cancelado el procesamiento del \_ gabinete.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: SPFILENOTIFY_FILEEXTRACTED mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56b5028dec11cf2317be080fb82b79bf155be007c66abcbee33492aa229d6317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665115"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ FILEEXTRACTED message

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) envía la notificación **SPFILENOTIFY \_ FILEEXTRACTED** a una rutina de devolución de llamada para indicar que se extrajo un archivo del gabinete o que se ha cancelado una extracción y se ha cancelado el procesamiento del gabinete.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información de ruta de acceso para el archivo extraído. El **miembro SourceFile** de la **estructura FILEPATHS** contiene la ruta de acceso de origen completa del archivador. El **miembro TargetFile** proporciona la ruta de acceso de destino completa del archivo que se va a instalar en el sistema.

</dd> <dt>

*Param2* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada del gabinete debe devolver uno de los valores siguientes.



| Código devuelto                                                                               | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NO \_ HAY NINGÚN ERROR**</dt> </dl>  | No se encontró ningún error, continúe procesando el gabinete.<br/>                                                                                                                                |
| <dl> <dt>**ERROR \_ XXX**</dt> </dl> | Error del tipo especificado. [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá cero. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error especificado.<br/> |



 

> [!Note]  
> No hay ninguna rutina de devolución de llamada de gabinete predeterminada proporcionada con la API de instalación. La aplicación de instalación debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por la [**función SetupIterateCabinet.**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

