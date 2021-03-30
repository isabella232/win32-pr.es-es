---
description: El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces ITTerminal y ITMultiTrackTerminal. Estos objetos también exponen la interfaz ITMediaControl, que proporciona métodos para detener, iniciar y navegar por los elementos multimedia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de reproducción de archivos y terminal de grabación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001930"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="72cc7-104">Terminal de reproducción de archivos y terminal de grabación de archivos</span><span class="sxs-lookup"><span data-stu-id="72cc7-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="72cc7-105">El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) y [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) .</span><span class="sxs-lookup"><span data-stu-id="72cc7-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="72cc7-106">Estos objetos también exponen la interfaz [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , que proporciona métodos para detener, iniciar y navegar por los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="72cc7-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="72cc7-107">El terminal de reproducción de archivos expone la interfaz [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , que tiene métodos específicos de reproducción.</span><span class="sxs-lookup"><span data-stu-id="72cc7-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="72cc7-108">El terminal de grabación de archivos expone la interfaz [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , que proporciona métodos específicos del registro.</span><span class="sxs-lookup"><span data-stu-id="72cc7-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="72cc7-109">Como [terminales multipista](multitrack-terminals.md), el terminal de grabación de archivos y el terminal de reproducción de archivos administran una colección de [terminales de seguimiento](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="72cc7-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
