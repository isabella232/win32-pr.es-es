---
description: Normalmente, las marcas de tiempo se incluyen cuando se firma un archivo mediante SignTool con la opción-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Agregar marcas de tiempo a archivos firmados anteriormente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105670213"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="7e818-103">Agregar marcas de tiempo a archivos firmados anteriormente</span><span class="sxs-lookup"><span data-stu-id="7e818-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="7e818-104">Normalmente, las marcas de tiempo se incluyen cuando se firma un archivo mediante SignTool con la opción **-t** .</span><span class="sxs-lookup"><span data-stu-id="7e818-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="7e818-105">Además, se pueden agregar marcas de tiempo a archivos firmados sin una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7e818-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="7e818-106">El comando siguiente agrega una marca de tiempo a un archivo firmado anteriormente:</span><span class="sxs-lookup"><span data-stu-id="7e818-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="7e818-107">**SignTool timestamp-t https: \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="7e818-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="7e818-108">El archivo que se va a marcar para la marca de tiempo debe haberse firmado previamente.</span><span class="sxs-lookup"><span data-stu-id="7e818-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="7e818-109">Para obtener más información sobre SignTool, consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="7e818-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



