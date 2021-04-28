---
description: La regla general es que una aplicación de escritorio puede llamar a Windows Runtime API (WinRT). Sin embargo, algunas API, incluidas las API de interfaz de usuario XAML, requieren que la aplicación que realiza la llamada tenga una identidad de paquete.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API de WinRT a las que se puede llamar desde una aplicación de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172487"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a><span data-ttu-id="3b6ef-104">API de WinRT a las que se puede llamar desde una aplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="3b6ef-104">WinRT APIs callable from a desktop app</span></span>

<span data-ttu-id="3b6ef-105">La [mayoría Windows Runtime api de escritorio (WinRT)](/uwp/api/) se pueden usar en aplicaciones de escritorio (.NET y C++) nativas.</span><span class="sxs-lookup"><span data-stu-id="3b6ef-105">Most [Windows Runtime (WinRT) APIs](/uwp/api/) can be used by desktop (.NET and native C++) apps.</span></span> <span data-ttu-id="3b6ef-106">Sin embargo, algunas clases de WinRT están diseñadas para y solo se admiten para su uso en aplicaciones para UWP.</span><span class="sxs-lookup"><span data-stu-id="3b6ef-106">However, some WinRT classes are designed for and are only supported for use in UWP apps.</span></span> <span data-ttu-id="3b6ef-107">Esto incluye [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)y algunas clases relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3b6ef-107">This includes [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview), and some related classes.</span></span> <span data-ttu-id="3b6ef-108">Otras clases de WinRT funcionan en aplicaciones de escritorio, excepto para miembros específicos.</span><span class="sxs-lookup"><span data-stu-id="3b6ef-108">Other WinRT classes work in desktop apps except for specific members.</span></span>

<span data-ttu-id="3b6ef-109">Para obtener más información, [consulte Windows Runtime API no admitidas en aplicaciones de escritorio.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api)</span><span class="sxs-lookup"><span data-stu-id="3b6ef-109">For more information, see [Windows Runtime APIs not supported in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span></span> <span data-ttu-id="3b6ef-110">Si está disponible, en este artículo se sugieren API alternativas para lograr la misma funcionalidad que las API no admitidas.</span><span class="sxs-lookup"><span data-stu-id="3b6ef-110">Where available, this article suggests alternative APIs to achieve the same functionality as the unsupported APIs.</span></span>
