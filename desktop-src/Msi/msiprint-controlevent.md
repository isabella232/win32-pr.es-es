---
description: Este evento está publicado por el control ScrollableText para permitir que el usuario imprima el contenido de ese control.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913262"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="02c0a-103">MsiPrint ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="02c0a-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="02c0a-104">Este evento está publicado por el [control ScrollableText](scrollabletext-control.md) para permitir que el usuario imprima el contenido de ese control.</span><span class="sxs-lookup"><span data-stu-id="02c0a-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="02c0a-105">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="02c0a-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="02c0a-106">Este ControlEvent, está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="02c0a-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="02c0a-107">Un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el [control ScrollableText](scrollabletext-control.md)debe suscribirse a este evento.</span><span class="sxs-lookup"><span data-stu-id="02c0a-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="02c0a-108">TheMsiPrint ControlEvent, se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="02c0a-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="02c0a-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="02c0a-109">Published By</span></span>

[<span data-ttu-id="02c0a-110">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="02c0a-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="02c0a-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="02c0a-111">Argument</span></span>

<span data-ttu-id="02c0a-112">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="02c0a-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="02c0a-113">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="02c0a-113">Action on Subscribers</span></span>

<span data-ttu-id="02c0a-114">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="02c0a-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="02c0a-115">Uso típico</span><span class="sxs-lookup"><span data-stu-id="02c0a-115">Typical Use</span></span>

<span data-ttu-id="02c0a-116">Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo que el [control ScrollableText](scrollabletext-control.md) se puede usar para mostrar un cuadro de diálogo modal que permita al usuario imprimir el contenido del control ScrollableText.</span><span class="sxs-lookup"><span data-stu-id="02c0a-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



