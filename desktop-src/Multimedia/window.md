---
title: Window (comando)
description: El comando Window controla la ventana de presentación.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- comando de ventana multimedia de Windows
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490474"
---
# <a name="window-command"></a>Window (comando)

El comando Window controla la ventana de presentación. Puede usar este comando para cambiar las características de presentación de la ventana o proporcionar una ventana de destino para que el controlador use en lugar de la ventana de presentación predeterminada. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para controlar la ventana de presentación. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando de ventana y las marcas usadas por cada tipo.



| Value        | Significado                                                                                                                                        | Significado                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | administrar el estado de *hWnd* hidestate minimizestate restorestate showshow maximized                                                                    | Mostrar minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow NormalText *Caption*                                             |
| overlay      | fixedhandle defaulthandle *hWnd* State hidestate iconicstate maximizedstate minimizestate minimizedstate no actionstate noactivatestate normal | State restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *Caption* |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszWindowFlags** y su significado.



| Value                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fijo                            | Deshabilita la expansión de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| identificador predeterminado                   | Especifica que el dispositivo debe volver a establecer la ventana de presentación en la ventana predeterminada creada durante la operación de [apertura](open.md) . En el caso de los dispositivos de superposición de vídeo, especifica que el dispositivo debe crear y administrar su propia ventana de destino.                                                                                                                                                                                                                                                                                                                                                  |
| identificador *hWnd*                    | Especifica el identificador de la ventana de destino que se va a usar en lugar de la ventana predeterminada. El parámetro *hWnd* contiene el equivalente numérico ASCII del identificador de ventana devuelto por la función [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Dos instancias de dispositivo pueden usar el mismo identificador de ventana siempre que cada instancia actualice los píxeles de vídeo e imagen en la ventana como si la otra instancia no existiera. Cuando la salida de vídeo se deshabilita con [setvideo](setvideo.md) "OFF", un comando de [actualización](update.md) hará que el rectángulo de destino sea un color sólido. |
| Mostrar maximizado                   | Maximiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostrar [**min**](min.md) noactive | Muestra la ventana de destino como un icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Mostrar minimizado                   | Minimiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostrar na                          | Muestra la ventana de destino en su estado actual; la ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostrar noactivate                  | Muestra la ventana de destino en su tamaño y posición más recientes; la ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostrar normal                      | Activa y muestra la ventana de destino en su tamaño y posición originales. (Es lo mismo que la marca "State restore").                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ocultar estado                       | Oculta la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| icono de estado                     | Muestra la ventana de destino como un icono.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Estado maximizado                  | Maximiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| minimizar estado                   | Minimiza la ventana de destino y activa la ventana de nivel superior en la lista del administrador de ventanas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Estado minimizado                  | Minimiza la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| no acción de estado                  | Muestra la ventana de destino en su estado actual. La ventana que está activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Estado noactivate                 | Muestra la ventana de destino en su tamaño y estado más recientes. La ventana activa actualmente permanece activa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| estado normal                     | Activa y muestra la ventana de destino en su tamaño y posición originales.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| restauración de estado                    | Activa y muestra la ventana de destino en su tamaño y posición originales.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Mostrar estado                       | Muestra la ventana de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ajustar                          | Habilita la expansión de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| *título* de texto                   | Especifica el título de la ventana de destino. Si este texto contiene espacios en blanco incrustados, todo el título debe estar entre comillas. El título predeterminado de la ventana predeterminada está en blanco.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Normalmente, los dispositivos de superposición de vídeo crean y muestran una ventana cuando se abren. Si la aplicación proporciona una ventana al controlador, la aplicación es responsable de administrar los mensajes enviados a la ventana.

Dado que puede usar el comando [status](status.md) para recuperar el identificador de la ventana de visualización del controlador, también puede usar las funciones de administrador de ventanas estándar (como [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) para manipular la ventana.

## <a name="examples"></a>Ejemplos

El siguiente comando muestra y establece el título de la ventana de reproducción de la "película".

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[reproducción](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

