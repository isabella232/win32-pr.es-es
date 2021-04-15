---
description: La \_ notificación SPFILENOTIFY FILEINCABINET se envía a una rutina de devolución de llamada por SetupIterateCabinet para cada archivo que se encuentra en el archivo. cab. La rutina de devolución de llamada debe devolver un valor que indica si se va a extraer el archivo.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Mensaje de SPFILENOTIFY_FILEINCABINET (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669783"
---
# <a name="spfilenotify_fileincabinet-message"></a>SPFILENOTIFY \_ FILEINCABINET

La notificación **SPFILENOTIFY \_ FILEINCABINET** se envía a una rutina de devolución de llamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para cada archivo que se encuentra en el archivo. cab. La rutina de devolución de llamada debe devolver un valor que indica si se va a extraer el archivo.


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a un [**archivo \_ en la estructura de \_ \_ información de contenedor**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) que contiene información sobre el archivo en el archivo. cab.

</dd> <dt>

*Param2* 
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de archivo del archivo. cab.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los siguientes.



| Código devuelto                                                                                 | Descripción                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl> | No extraiga el archivo, omítalo.<br/> |
| <dl> <dt>**FILEOP \_ Doit**</dt> </dl> | Extrae el archivo.<br/>                 |



 

Si la rutina de devolución de llamada devuelve FILEOP \_ doit, el nombre que se va a usar para el archivo extraído debe especificarse en el miembro **FullTargetName** del [**archivo en la estructura \_ de \_ \_ información de contenedor**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) pasada a la rutina en *parám1*.

> [!Note]  
> No hay ninguna rutina de devolución de llamada del archivo. cab predeterminada. La aplicación de instalación debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

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

[**ARCHIVO \_ en \_ información de contenedor \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




