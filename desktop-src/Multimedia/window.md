---
title: comando window
description: El comando de ventana controla la ventana de presentación.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- comando window Windows Multimedia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370142"
---
# <a name="window-command"></a>comando window

El comando de ventana controla la ventana de presentación. Puede usar este comando para cambiar las características de presentación de la ventana o proporcionar una ventana de destino para que el controlador la use en lugar de la ventana de presentación predeterminada. Los dispositivos de superposición de vídeo y vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Marca para controlar la ventana de presentación. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando de ventana y las marcas usadas por cada tipo.



| Value        | Significado                                                                                                                                        | Significado                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | handle *hwnd* state hidestate minimizestate restorestate showshow maximized                                                                    | show minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normaltext *caption*                                             |
| overlay      | fixedhandle defaulthandle hwnd state *hidestate* iconicstate maximizedstate minimizestate minimizedstate no actionstate noactivatestate normal | state restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *caption* |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszWindowFlags** y sus significados.



| Value                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fijo                            | Deshabilita la extensión de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| identificador predeterminado                   | Especifica que el dispositivo debe volver a establecer la ventana de presentación en la ventana predeterminada creada durante la [operación de](open.md) apertura. En el caso de los dispositivos de superposición de vídeo, especifica que el dispositivo debe crear y administrar su propia ventana de destino.                                                                                                                                                                                                                                                                                                                                                  |
| handle *hwnd*                    | Especifica el identificador de la ventana de destino que se usará en lugar de la ventana predeterminada. El *parámetro hwnd* contiene el equivalente numérico ASCII del identificador de ventana devuelto por la [función CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Dos instancias de dispositivo pueden usar el mismo identificador de ventana siempre que cada instancia actualice los píxeles de imagen y vídeo de la ventana como si la otra instancia no existiera. Cuando la salida de vídeo está deshabilitada [con setvideo](setvideo.md) "off", un comando [update](update.md) hará que el rectángulo de destino sea un color sólido. |
| mostrar maximizado                   | Maximiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show [**min**](min.md) noactive | Muestra la ventana de destino como un icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| mostrar minimizado                   | Minimiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show na                          | Muestra la ventana de destino en su estado actual; la ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| show noactivate                  | Muestra la ventana de destino en su tamaño y posición más recientes; la ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| mostrar normal                      | Activa y muestra la ventana de destino en su tamaño y posición originales. (Esto es lo mismo que la marca de "restauración de estado").                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| state hide                       | Oculta la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| icono de estado                     | Muestra la ventana de destino como un icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| estado maximizado                  | Maximiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| minimización de estado                   | Minimiza la ventana de destino y activa la ventana de nivel superior en la lista del administrador de ventanas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| estado minimizado                  | Minimiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| state no action                  | Muestra la ventana de destino en su estado actual. La ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| state noactivate                 | Muestra la ventana de destino en su tamaño y estado más recientes. La ventana activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| state normal                     | Activa y muestra la ventana de destino en su tamaño y posición originales.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| restauración de estado                    | Activa y muestra la ventana de destino en su tamaño y posición originales.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| state show                       | Muestra la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ajustar                          | Habilita el stretching de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| título de *texto*                   | Especifica el título de la ventana de destino. Si este texto contiene espacios en blanco incrustados, todo el título debe incluirse entre comillas. El título predeterminado de la ventana predeterminada está en blanco.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los dispositivos de superposición de vídeo suelen crear y mostrar una ventana cuando se abren. Si la aplicación proporciona una ventana al controlador, la aplicación es responsable de administrar los mensajes enviados a la ventana.

Dado que puede usar el comando [status](status.md) para recuperar el identificador en la ventana de presentación del controlador, también puede usar las funciones estándar del administrador de ventanas (como [ShowWindow)](/windows/win32/api/winuser/nf-winuser-showwindow)para manipular la ventana.

## <a name="examples"></a>Ejemplos

El comando siguiente muestra y establece el título de la ventana de reproducción de "película".

``` syntax
window movie text "Welcome to the Movies" state show
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[Jugar](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

