---
description: Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se pasa de nuevo al administrador de trabajos de impresión.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de Puerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706639"
---
# <a name="port-monitors"></a><span data-ttu-id="78895-103">Monitores de Puerto</span><span class="sxs-lookup"><span data-stu-id="78895-103">Port Monitors</span></span>

<span data-ttu-id="78895-104">Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se pasa de nuevo al administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="78895-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="78895-105">El administrador de trabajos de impresión envía estos comandos de bajo nivel a un monitor.</span><span class="sxs-lookup"><span data-stu-id="78895-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="78895-106">Un monitor de puerto es un archivo. dll que pasa los comandos de dispositivo sin formato a través de la red, a través de un puerto paralelo o a través de un puerto serie al dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="78895-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="78895-107">Se pueden instalar monitores de Puerto personalizados para permitir el paso de datos del dispositivo a través de otros puertos de comunicación.</span><span class="sxs-lookup"><span data-stu-id="78895-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="78895-108">Utilice las siguientes funciones para trabajar con monitores de puerto.</span><span class="sxs-lookup"><span data-stu-id="78895-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="78895-109">Función</span><span class="sxs-lookup"><span data-stu-id="78895-109">Function</span></span>                               | <span data-ttu-id="78895-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78895-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="78895-111">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="78895-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="78895-112">Instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.</span><span class="sxs-lookup"><span data-stu-id="78895-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="78895-113">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="78895-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="78895-114">Quita un monitor de Puerto agregado por la función [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="78895-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="78895-115">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="78895-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="78895-116">Enumera los monitores de Puerto instalados en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="78895-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



