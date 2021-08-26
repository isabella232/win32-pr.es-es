---
description: Información general sobre cómo mostrar el panel de entrada.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Mostrar el panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940795"
---
# <a name="displaying-the-input-panel"></a>Mostrar el panel de entrada

\[[**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) [(Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) para código administrado). Consulte Programar el [panel de entrada de texto](programming-the-text-input-panel.md).\]

El orden de los distintos eventos de foco para un control es el siguiente:

-   [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control.Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control.Validating](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control.Validated](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control.LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

No hay ninguna garantía de que el control tenga realmente el foco en el momento en que se escribe la propiedad [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) cuando se establece en el controlador de eventos [Control.Enter.](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) El evento Control.Enter es el mejor lugar para asociar el objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un control, pero el evento [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) es el mejor lugar para cambiar la [propiedad PenInputPanel.Visible.](/previous-versions/ms571984(v=vs.100))

 

 
