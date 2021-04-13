---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487691"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Muestra la ventana Propiedades de carácter predeterminado.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada x de la ventana en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y de la ventana en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Marca de posición predeterminada. Si este parámetro es **true**, el agente de Microsoft muestra la ventana de la hoja de propiedades para el carácter predeterminado en la última ubicación que aparecía.

> [!Note]  
> En Windows 2000, puede que sea necesario llamar a la nueva API de [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) para asegurarse de que esta ventana se convierte en la ventana de primer plano. Para obtener más información sobre cómo establecer la ventana de primer plano en Windows 2000, vea la documentación del SDK de la plataforma.

 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 