---
description: La regla general es que una aplicación de escritorio puede llamar a una API Windows Runtime (WinRT). Sin embargo, algunas API, incluidas las API de interfaz de usuario XAML, requieren que la aplicación que realiza la llamada tenga una identidad de paquete.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API de WinRT a las que se puede llamar desde una aplicación de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130307"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API de WinRT a las que se puede llamar desde una aplicación de escritorio

La [mayoría Windows api de runtime (WinRT) se](/uwp/api/) pueden usar en aplicaciones de escritorio (.NET y C++) nativas. Sin embargo, algunas clases de WinRT están diseñadas para y solo se admiten para su uso en aplicaciones para UWP. Esto incluye [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)y algunas clases relacionadas. Otras clases de WinRT funcionan en aplicaciones de escritorio, excepto para miembros específicos.

Para obtener más información, consulte [API de Windows Runtime disponibles para aplicaciones de escritorio](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Cuando están disponibles, en este artículo se sugieren API alternativas para lograr la misma funcionalidad que con las API no admitidas.
