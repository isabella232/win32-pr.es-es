---
description: Describe cómo crear un objeto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Creación de un objeto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696138"
---
# <a name="creating-a-peninputpanel-object"></a>Creación de un objeto PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) y por [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)). Consulte el panel de [entrada de texto Programming](programming-the-text-input-panel.md).\]

Los constructores de código administrado proporcionan una forma cómoda de crear un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) y adjuntarlo a un control en un solo paso. En este ejemplo de C se \# crea un objeto PenInputPanel y se asocia a un control [InkEdit](/previous-versions/ms835842(v=msdn.10)) existente, `InkEdit1` , con una línea de código.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



El mismo ejemplo en Visual Basic .NET tiene el siguiente aspecto:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Esta técnica es útil en los casos en los que un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) se asociará a un solo control a lo largo de su duración. En los casos en los que desee usar un objeto PenInputPanel y asociarlo a varios controles, como se muestra en el [ejemplo PenInputPanel](peninputpanel-sample.md), use la propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) para cambiar el control al que está asociado el objeto PenInputPanel.

Para asociar un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un control sin usar un constructor, use la propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) . Utilice esta técnica para los lenguajes que no admiten los constructores administrados, como C++.

 

 
