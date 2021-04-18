---
description: Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Datos de formato mostrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540219"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="f196b-103">Datos de formato mostrados</span><span class="sxs-lookup"><span data-stu-id="f196b-103">Formatting Displayed Data</span></span>

<span data-ttu-id="f196b-104">Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="f196b-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="f196b-105">Monitor de red proporciona un formateador genérico que proporciona los servicios básicos necesarios para mostrar la mayoría de los tipos de datos que existen dentro de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="f196b-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="f196b-106">Sin embargo, el formateador genérico no admite todos los tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="f196b-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="f196b-107">Por ejemplo, el formateador genérico no admite lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f196b-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="f196b-108">Varios tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f196b-108">Several address types.</span></span>
-   <span data-ttu-id="f196b-109">Nombres descriptivos de origen y destino.</span><span class="sxs-lookup"><span data-stu-id="f196b-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="f196b-110">Identificadores de objetos.</span><span class="sxs-lookup"><span data-stu-id="f196b-110">Object identifiers.</span></span>
-   <span data-ttu-id="f196b-111">Tipos de datos enteros grandes.</span><span class="sxs-lookup"><span data-stu-id="f196b-111">Large integer data types.</span></span>
-   <span data-ttu-id="f196b-112">Tipos de datos enteros de longitud variable pequeños.</span><span class="sxs-lookup"><span data-stu-id="f196b-112">Variable length small integer data types.</span></span>

<span data-ttu-id="f196b-113">En el ejemplo siguiente se identifican dos cadenas con formato para la propiedad ID. de privilegio.</span><span class="sxs-lookup"><span data-stu-id="f196b-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="f196b-114">La primera línea de código muestra la salida del formateador genérico.</span><span class="sxs-lookup"><span data-stu-id="f196b-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="f196b-115">El resultado se basa en el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f196b-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="f196b-116">En la segunda línea de código se muestra la salida de un formateador personalizado con una cadena para los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f196b-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="f196b-117">Cuando sea posible, use el formateador genérico para mostrar los datos porque le permite controlar el tamaño de la DLL del analizador y proporciona mejores capacidades multiplataforma para el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="f196b-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



