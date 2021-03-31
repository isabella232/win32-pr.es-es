---
title: Compatibilidad con Unicode para controles comunes
description: En este tema se describe cómo admitir Unicode para las notificaciones de control comunes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995752"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="5eb5b-103">Compatibilidad con Unicode para controles comunes</span><span class="sxs-lookup"><span data-stu-id="5eb5b-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="5eb5b-104">En este tema se describe cómo admitir Unicode para las notificaciones de control comunes.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="5eb5b-105">En las versiones 5,80 y posteriores de comctl32.dll, las notificaciones de controles comunes admiten los formatos ANSI y Unicode en sistemas Windows 95 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="5eb5b-106">El sistema determina el formato que se va a usar mediante el envío de la ventana a un mensaje de [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb5b-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="5eb5b-107">Para especificar un formato, devuelve \_ ANSI de NFR para las notificaciones ANSI o \_ Unicode NFR para las notificaciones Unicode.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="5eb5b-108">Si no controla este mensaje, el sistema llama a [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar el formato.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="5eb5b-109">Dado que Windows 95 y Windows 98 siempre devuelven **false** a esta llamada de función, usan notificaciones ANSI de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb5b-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5eb5b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb5b-111">Acerca de los controles comunes</span><span class="sxs-lookup"><span data-stu-id="5eb5b-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 