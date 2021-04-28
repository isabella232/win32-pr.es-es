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
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API de WinRT a las que se puede llamar desde una aplicación de escritorio

La [mayoría Windows Runtime api de escritorio (WinRT)](/uwp/api/) se pueden usar en aplicaciones de escritorio (.NET y C++) nativas. Sin embargo, algunas clases de WinRT están diseñadas para y solo se admiten para su uso en aplicaciones para UWP. Esto incluye [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)y algunas clases relacionadas. Otras clases de WinRT funcionan en aplicaciones de escritorio, excepto para miembros específicos.

Para obtener más información, [consulte Windows Runtime API no admitidas en aplicaciones de escritorio.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api) Si está disponible, en este artículo se sugieren API alternativas para lograr la misma funcionalidad que las API no admitidas.
