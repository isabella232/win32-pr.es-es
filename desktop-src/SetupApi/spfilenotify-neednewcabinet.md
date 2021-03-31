---
description: La notificación de NEEDNEWCABINET de SPFILENOTIFY \_ se envía mediante SetupIterateCabinet para indicar que el archivo actual continúa en otro contenedor.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Mensaje de SPFILENOTIFY_NEEDNEWCABINET (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278981"
---
# <a name="spfilenotify_neednewcabinet-message"></a>SPFILENOTIFY \_ NEEDNEWCABINET

La notificación de **\_ NEEDNEWCABINET de SPFILENOTIFY** se envía mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que el archivo actual continúa en otro contenedor. A continuación, la rutina de devolución de llamada puede llamar a [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)o crear su propio cuadro de diálogo para solicitar al usuario que inserte el siguiente disco.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura de [**\_ información**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) del archivo. cab que contiene información sobre el contenedor y el archivo que se va a extraer.

</dd> <dt>

*Param2* 
</dt> <dd>

Si la devolución de llamada NO devuelve ningún \_ error, este parámetro es un puntero a una cadena terminada en NULL. Si la cadena no está vacía, especifica una nueva ruta de acceso al archivo. cab.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina debe devolver uno de los valores siguientes.



| Código devuelto                                                                                 | Descripción                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SIN \_ errores**</dt> </dl>    | No se encontró ningún error y continúe procesando el archivo. cab.<br/>                                                                                                                                                                        |
| <dl> <dt>**Error \_* de XXX * * *</dt> </dl> | Se produjo un error del tipo especificado. La función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá **false** y el código de error especificado será devuelto por una llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).<br/> |



 

> [!Note]  
> No hay ninguna rutina de devolución de llamada del archivo. cab predeterminada; por lo tanto, debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="remarks"></a>Observaciones

Si la rutina de devolución de llamada NO devuelve ningún \_ error, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) comprueba el búfer señalado por *parám2*. Si el búfer no está vacío, contiene una nueva ruta de acceso de origen. Si el búfer está vacío, se supone que la ruta de acceso de origen no ha cambiado.

La función de devolución de llamada debe asegurarse de que el archivo. cab es accesible antes de que vuelva, llamando a la función [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , en caso de que sea necesario insertar nuevos medios.

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

[**información del archivo. cab \_**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

