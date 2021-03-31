---
description: Los monitores se pueden configurar mediante la interfaz de usuario de Monitor de red. Los usuarios finales pueden pasar los criterios de configuración al monitor mediante un formulario HTML almacenado como un archivo HTM en la subcarpeta siguiente del SDK de Monitor de red instalado.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Configuración de monitor (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001231"
---
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="c0a17-104">Configuración de monitor (Monitor de red)</span><span class="sxs-lookup"><span data-stu-id="c0a17-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="c0a17-105">Los monitores se pueden configurar mediante la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c0a17-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="c0a17-106">Los usuarios finales pueden pasar los criterios de configuración al monitor mediante un formulario HTML almacenado como un archivo HTM en la subcarpeta siguiente del SDK de Monitor de red instalado.</span><span class="sxs-lookup"><span data-stu-id="c0a17-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="c0a17-107">Cuando un usuario final selecciona el botón **establecer configuración de monitor** , el explorador genera un mensaje **post** HTML, que incluye los nombres y los valores de todos los elementos de formulario HTML.</span><span class="sxs-lookup"><span data-stu-id="c0a17-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="c0a17-108">Cuando el MCSVC llama al método [IMonitor::D oconfigure](imonitor-doconfigure.md) , el parámetro *pConfiguration* apunta a los datos del mensaje post.</span><span class="sxs-lookup"><span data-stu-id="c0a17-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="c0a17-109">En el ejemplo de código siguiente se proporciona un ejemplo de datos POST Message:</span><span class="sxs-lookup"><span data-stu-id="c0a17-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Estos datos se pasan como una cadena ASCII larga. La cadena tiene un aspecto peculiar, tanto para su longitud como para la apariencia de secciones como% 3A% 5C y% 0D% 0A. Esta peculiaridad está causada por HTML, que requiere que un método ponga todas las cadenas posibles de ANSI, DBCS y Unicode en un formato ASCII. Por ejemplo, el método **Conconfigure** inserta ciertos caracteres, como la y comercial (&) delante de cada nombre de variable para identificarlo como un nombre de variable. % 3A% 5C es un formato codificado del carácter de dos puntos y% 0D% 0A indica un par de retorno de carro/avance de carro. <span data-ttu-id="c0a17-115">En el siguiente código de ejemplo se proporciona el código HTML resultante como interpretado por el monitor.</span><span class="sxs-lookup"><span data-stu-id="c0a17-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



