---
description: Describe el uso del objeto PenInputPanel con cuadros combinados.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Uso de PenInputPanel con cuadros combinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1e90d581e08f9a23346bbf13cf8c3866f6e947f1d9b23375248f3ba9c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589305"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Uso de PenInputPanel con cuadros combinados

\[El [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) se ha reemplazado por [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)). Consulte Programar el [panel de entrada de texto](programming-the-text-input-panel.md).\]

Si adjunta un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a un control [ComboBox,](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) pulse el lápiz de tableta en el cuadro combinado de la parte del control de edición en tiempo de ejecución, el objeto PenInputPanel no aparecerá. Sin embargo, aparece si pulsa en la flecha desplegable. Esto se debe a que la ventana del control de edición del cuadro combinado no es la ventana que recibe mensajes de lápiz. Los cuadros combinados tienen una ventana de edición secundaria. La solución a este problema es determinar si la ventana a la que está asociado el objeto PenInputPanel tiene una ventana secundaria. Si es así, puede adjuntar el objeto PenInputPanel a la ventana secundaria.

Establecer la [propiedad VerticalOffset](/previous-versions/ms571983(v=vs.100)) del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) en un valor de -1 hace que el panel aparezca en la parte superior del cuadro combinado.

 

 
