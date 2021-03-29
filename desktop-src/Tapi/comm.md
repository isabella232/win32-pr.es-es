---
description: La clase de dispositivo COMM se compone de puertos de comunicaciones. Puede tener acceso a estos dispositivos mediante las funciones de archivo y de comunicaciones.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810898"
---
# <a name="comm"></a><span data-ttu-id="77905-104">com</span><span class="sxs-lookup"><span data-stu-id="77905-104">comm</span></span>

<span data-ttu-id="77905-105">La clase de dispositivo COMM se compone de puertos de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="77905-105">The comm device class consists of communications ports.</span></span> <span data-ttu-id="77905-106">Puede tener acceso a estos dispositivos mediante las funciones de [archivo](/windows/desktop/FileIO/file-management-functions) y de [comunicaciones](/windows/desktop/DevIO/communications-functions).</span><span class="sxs-lookup"><span data-stu-id="77905-106">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span>

<span data-ttu-id="77905-107">La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el valor de \_ ASCII STRINGFORMAT y anexando una cadena terminada en null que especifica el nombre del dispositivo de comunicación (por ejemplo, el nombre del módem).</span><span class="sxs-lookup"><span data-stu-id="77905-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_ASCII value and appending a null-terminated string that specifies the name of the communication device (such as the modem name).</span></span>

 

 
