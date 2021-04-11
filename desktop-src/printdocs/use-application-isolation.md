---
description: Las aplicaciones pueden declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de las aplicaciones.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Cómo: utilizar el aislamiento de aplicaciones'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276771"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="6a951-103">Cómo: utilizar el aislamiento de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6a951-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="6a951-104">Las aplicaciones pueden declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislar la aplicación del controlador de impresora y mejorar la confiabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a951-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="6a951-105">El servicio de impresión de Windows permite que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="6a951-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="6a951-106">Con esta característica, la aplicación impide que se bloquee en caso de que se produzca un error en el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="6a951-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="6a951-107">El aislamiento del controlador de impresora se implementa en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6a951-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6a951-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6a951-108">Prerequisites</span></span>

-   <span data-ttu-id="6a951-109">Una aplicación de código administrado o de la tienda Windows que usa la impresión de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a951-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="6a951-110">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="6a951-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="6a951-111">Actualización del manifiesto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6a951-111">Update the app manifest</span></span>

<span data-ttu-id="6a951-112">Para habilitar el aislamiento del controlador de impresora, es necesario agregar el elemento **printerDriverIsolation** al manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a951-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="6a951-113">A continuación se muestra cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="6a951-113">Here's how:</span></span>

1.  <span data-ttu-id="6a951-114">Edite el manifiesto de la aplicación, agregando el elemento **printerDriverIsolation** con un valor de **true** al elemento **windowsSettings** del elemento **Application** , como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6a951-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="6a951-115">Vuelva a compilar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a951-115">Rebuild your app.</span></span>

 

 



