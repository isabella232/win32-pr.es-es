---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362cffa8d4b34d70111505a60fd5eadc68a220cd45c3beb519e5e39ba62f1a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749819"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Muestra la ventana de propiedades de caracteres predeterminadas.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x de la ventana en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada Y de la ventana en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Marca de posición predeterminada. Si este parámetro es **True,** Microsoft Agent muestra la ventana de hoja de propiedades del carácter predeterminado en la última ubicación en la que apareció.

> [!Note]  
> Para Windows 2000, puede ser necesario llamar a la nueva API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) para asegurarse de que esta ventana se convierte en la ventana de primer plano. Para obtener más información sobre cómo establecer la ventana de primer plano Windows 2000, consulte la documentación de Platform SDK.

 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 