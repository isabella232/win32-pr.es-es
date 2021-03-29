---
title: Búsqueda asincrónica
description: El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas. Las búsquedas asincrónicas devuelven el control a la aplicación que realiza la llamada inmediatamente.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994505"
---
# <a name="asynchronous-searching"></a>Búsqueda asincrónica

El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas. Las búsquedas asincrónicas devuelven el control a la aplicación que realiza la llamada inmediatamente. A continuación, se notifica a la aplicación sobre cada dispositivo individual a medida que se encuentra, mediante una interfaz de devolución de llamada que la aplicación ha registrado.

La búsqueda asincrónica es mejor para las interfaces de usuario gráficas y para las aplicaciones que realizan la supervisión continua.

La estructura general de una búsqueda asincrónica es:

1.  Crear un objeto de búsqueda
2.  Inicio de la búsqueda
3.  Reciba notificaciones de devolución de llamada y realice los pasos de procesamiento adecuados.
4.  Cuando la búsqueda ya no sea necesaria, cancele la búsqueda y libere los objetos asociados.

> [!Note]  
> En el código de devolución de llamada, una aplicación no puede liberar el objeto del que recibe notificaciones, como un nuevo dispositivo, ni puede cancelar la búsqueda.

 

## <a name="c-example"></a>Ejemplo de C++

Las aplicaciones de C++ deben implementar un objeto de devolución de llamada para pasarlo a la búsqueda. Vea [Buscar de forma asincrónica en C++](searching-asynchronously-in-c-.md) para ver el código de ejemplo que muestra esta acción.

## <a name="vbscript-example"></a>Ejemplo de VBScript

El código de VBScript debe pasar la dirección de la función de devolución de llamada.


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




