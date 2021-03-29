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
# <a name="asynchronous-searching"></a><span data-ttu-id="47c13-104">Búsqueda asincrónica</span><span class="sxs-lookup"><span data-stu-id="47c13-104">Asynchronous Searching</span></span>

<span data-ttu-id="47c13-105">El objeto de buscador de dispositivos habilita las búsquedas sincrónicas y asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="47c13-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="47c13-106">Las búsquedas asincrónicas devuelven el control a la aplicación que realiza la llamada inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="47c13-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="47c13-107">A continuación, se notifica a la aplicación sobre cada dispositivo individual a medida que se encuentra, mediante una interfaz de devolución de llamada que la aplicación ha registrado.</span><span class="sxs-lookup"><span data-stu-id="47c13-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="47c13-108">La búsqueda asincrónica es mejor para las interfaces de usuario gráficas y para las aplicaciones que realizan la supervisión continua.</span><span class="sxs-lookup"><span data-stu-id="47c13-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="47c13-109">La estructura general de una búsqueda asincrónica es:</span><span class="sxs-lookup"><span data-stu-id="47c13-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="47c13-110">Crear un objeto de búsqueda</span><span class="sxs-lookup"><span data-stu-id="47c13-110">Create a search object</span></span>
2.  <span data-ttu-id="47c13-111">Inicio de la búsqueda</span><span class="sxs-lookup"><span data-stu-id="47c13-111">Start the search</span></span>
3.  <span data-ttu-id="47c13-112">Reciba notificaciones de devolución de llamada y realice los pasos de procesamiento adecuados.</span><span class="sxs-lookup"><span data-stu-id="47c13-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="47c13-113">Cuando la búsqueda ya no sea necesaria, cancele la búsqueda y libere los objetos asociados.</span><span class="sxs-lookup"><span data-stu-id="47c13-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="47c13-114">En el código de devolución de llamada, una aplicación no puede liberar el objeto del que recibe notificaciones, como un nuevo dispositivo, ni puede cancelar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="47c13-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="47c13-115">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="47c13-115">C++ Example</span></span>

<span data-ttu-id="47c13-116">Las aplicaciones de C++ deben implementar un objeto de devolución de llamada para pasarlo a la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="47c13-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="47c13-117">Vea [Buscar de forma asincrónica en C++](searching-asynchronously-in-c-.md) para ver el código de ejemplo que muestra esta acción.</span><span class="sxs-lookup"><span data-stu-id="47c13-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="47c13-118">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="47c13-118">VBScript Example</span></span>

<span data-ttu-id="47c13-119">El código de VBScript debe pasar la dirección de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="47c13-119">VBScript code must pass the address of the callback function.</span></span>


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



 

 




