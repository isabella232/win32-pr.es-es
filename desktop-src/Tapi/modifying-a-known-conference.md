---
description: En el fragmento de código siguiente se muestra la modificación de un intervalo de tiempo de conferencias. El intervalo de tiempo predeterminado es de treinta minutos. En este fragmento, el intervalo de tiempo se establece en un año.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modificación de una conferencia conocida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275173"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="820ac-105">Modificación de una conferencia conocida</span><span class="sxs-lookup"><span data-stu-id="820ac-105">Modifying a Known Conference</span></span>

<span data-ttu-id="820ac-106">\[Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="820ac-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="820ac-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="820ac-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="820ac-108">En el fragmento de código siguiente se muestra la modificación del intervalo de tiempo de una conferencia.</span><span class="sxs-lookup"><span data-stu-id="820ac-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="820ac-109">El intervalo de tiempo predeterminado es de treinta minutos.</span><span class="sxs-lookup"><span data-stu-id="820ac-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="820ac-110">En este fragmento, el intervalo de tiempo se establece en un año.</span><span class="sxs-lookup"><span data-stu-id="820ac-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="820ac-111">Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) y que se ha realizado una [enumeración de directorio de conferencia](enumerating-conference-directories.md) para obtener la entrada del directorio que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="820ac-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="820ac-112">Este fragmento también supone que no se trata de una conferencia de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="820ac-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="820ac-113">El cambio de las horas de una conferencia de multidifusión requiere la notificación del servidor de asignación de direcciones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="820ac-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="820ac-114">Vea [adquirir una dirección de multidifusión](acquiring-a-multicast-address.md) para obtener un ejemplo de cómo trabajar con el direccionamiento multidifusión.</span><span class="sxs-lookup"><span data-stu-id="820ac-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="820ac-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="820ac-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="820ac-116">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="820ac-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



