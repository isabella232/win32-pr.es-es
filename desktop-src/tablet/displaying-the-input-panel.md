---
description: Información general sobre cómo mostrar el panel de entrada.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Mostrar el panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707423"
---
# <a name="displaying-the-input-panel"></a>Mostrar el panel de entrada

\[[**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) para código administrado). Consulte el panel de [entrada de texto Programming](programming-the-text-input-panel.md).\]

El orden de los distintos eventos de foco para un control es el siguiente:

-   [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control. validando](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control. validado](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

No hay ninguna garantía de que el control realmente tenga el foco en el momento en que se escribe la propiedad [control. visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) cuando se establece en el controlador de eventos [control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) . El evento control. Enter es el mejor lugar para asociar el objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un control, pero el evento [control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) es el mejor lugar para cambiar la propiedad [PenInputPanel. visible](/previous-versions/ms571984(v=vs.100)) .

 

 
