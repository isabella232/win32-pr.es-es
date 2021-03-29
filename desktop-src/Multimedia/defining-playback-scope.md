---
title: Definir el ámbito de reproducción
description: Definir el ámbito de reproducción
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom (macro)
- MCIWndPlayTo (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994201"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="9b57b-105">Definir el ámbito de reproducción</span><span class="sxs-lookup"><span data-stu-id="9b57b-105">Defining Playback Scope</span></span>

<span data-ttu-id="9b57b-106">MCIWnd proporciona macros que permiten definir el *ámbito* de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9b57b-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="9b57b-107">El ámbito es la parte de la reproducción que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="9b57b-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="9b57b-108">Por ejemplo, puede reproducir el contenido de una posición distinta de la posición inicial mediante la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="9b57b-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="9b57b-109">Esta macro se mueve a la posición especificada, comienza la reproducción y continúa hasta el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="9b57b-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="9b57b-110">Del mismo modo, puede reproducir el contenido en un punto final especificado mediante la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="9b57b-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="9b57b-111">Esta macro se inicia en la posición de reproducción actual y se reproduce hasta que llega a la posición especificada o hasta que se alcanza el final del contenido, lo que suceda primero.</span><span class="sxs-lookup"><span data-stu-id="9b57b-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="9b57b-112">Además, puede definir las posiciones inicial y final mediante la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="9b57b-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="9b57b-113">Esta macro se mueve a la posición inicial especificada y se reproduce hasta que se alcanza la posición final especificada o el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="9b57b-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




