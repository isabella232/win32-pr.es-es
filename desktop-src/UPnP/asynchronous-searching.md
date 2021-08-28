---
title: Búsqueda asincrónica
description: El objeto Device Finder permite búsquedas sincrónicas y asincrónicas. Las búsquedas asincrónicas devuelven el control a la aplicación que realiza la llamada inmediatamente.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058143"
---
# <a name="asynchronous-searching"></a>Búsqueda asincrónica

El objeto Device Finder permite búsquedas sincrónicas y asincrónicas. Las búsquedas asincrónicas devuelven el control a la aplicación que realiza la llamada inmediatamente. A continuación, se notifica a la aplicación cada dispositivo individual cuando se encuentra, mediante una interfaz de devolución de llamada que la aplicación ha registrado.

La búsqueda asincrónica es mejor para las interfaces gráficas de usuario y las aplicaciones que realizan la supervisión continua.

La estructura general de una búsqueda asincrónica es:

1.  Creación de un objeto de búsqueda
2.  Inicio de la búsqueda
3.  Reciba notificaciones de devolución de llamada y siga los pasos de procesamiento adecuados.
4.  Cuando la búsqueda ya no sea necesaria, cancele la búsqueda y libere los objetos asociados.

> [!Note]  
> En el código de devolución de llamada, una aplicación no puede liberar el objeto sobre el que recibe la notificación, como un nuevo dispositivo, ni puede cancelar la búsqueda.

 

## <a name="c-example"></a>Ejemplo de C++

Las aplicaciones de C++ deben implementar un objeto de devolución de llamada para pasar a la búsqueda. Vea [Búsqueda asincrónica en C++ para obtener](searching-asynchronously-in-c-.md) código de ejemplo que ilustra esta acción.

## <a name="vbscript-example"></a>Ejemplo de VBScript

El código VBScript debe pasar la dirección de la función de devolución de llamada.


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



 

 




