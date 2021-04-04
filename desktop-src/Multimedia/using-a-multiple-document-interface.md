---
title: Usar una interfaz de varios documentos
description: Usar una interfaz de varios documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904572"
---
# <a name="using-a-multiple-document-interface"></a><span data-ttu-id="3e529-104">Usar una interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="3e529-104">Using a Multiple Document Interface</span></span>

<span data-ttu-id="3e529-105">Es posible que las aplicaciones que usan una interfaz de múltiples documentos (MDI) necesiten especificar estilos de ventana que no están disponibles a través de la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="3e529-105">Applications that use a multiple document interface (MDI) might need to specify window styles that are not available through the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="3e529-106">Para estas aplicaciones, puede registrar y crear una ventana MCIWnd mediante la función [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la función [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="3e529-106">For these applications, you can register and create an MCIWnd window by using the [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) function with the [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="3e529-107">La función **MCIWndRegisterClass** registra la \_ \_ clase de ventana de clase de ventana MCIWND y, a continuación, **CreateWindowEx** crea una instancia de una ventana de MCIWND.</span><span class="sxs-lookup"><span data-stu-id="3e529-107">The **MCIWndRegisterClass** function registers the MCIWND\_WINDOW\_CLASS window class and then **CreateWindowEx** creates an instance of an MCIWnd window.</span></span>

 

 