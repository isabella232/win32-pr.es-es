---
description: En el fragmento de código siguiente se muestra la enumeración de las conferencias en un servidor ILS especificado. Este fragmento supone que ya se ha realizado la conexión a un servidor ILS.
ms.assetid: da01c534-c700-4b4f-ac22-cede9930f80d
title: Enumerar directorios de conferencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eedffb44d92f52293dc9d1add8b53588503282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497812"
---
# <a name="enumerating-conference-directories"></a><span data-ttu-id="ba05d-104">Enumerar directorios de conferencia</span><span class="sxs-lookup"><span data-stu-id="ba05d-104">Enumerating Conference Directories</span></span>

<span data-ttu-id="ba05d-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba05d-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ba05d-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ba05d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ba05d-107">En el fragmento de código siguiente se muestra la enumeración de las conferencias en un servidor ILS especificado.</span><span class="sxs-lookup"><span data-stu-id="ba05d-107">The following code fragment illustrates the enumeration of conferences on a specified ILS server.</span></span> <span data-ttu-id="ba05d-108">Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) .</span><span class="sxs-lookup"><span data-stu-id="ba05d-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
SysFreeString( bNameToSearch );
```



## <a name="related-topics"></a><span data-ttu-id="ba05d-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba05d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba05d-110">**IEnumDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="ba05d-110">**IEnumDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)
</dt> </dl>

 

 



