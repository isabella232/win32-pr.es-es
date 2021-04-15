---
title: Cómo implementar la información sobre herramientas para los iconos de la barra de estado
description: Una manera no intrusiva de mostrar un mensaje explicativo para un icono de la barra de estado es implementar una información sobre herramientas. La información sobre herramientas desaparece al hacer clic en él, pero también puede especificar un valor de tiempo de espera.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488362"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Cómo implementar la información sobre herramientas para los iconos de la barra de estado

Una manera no intrusiva de mostrar un mensaje explicativo para un icono de la barra de estado es implementar una información sobre herramientas. La información sobre herramientas desaparece al hacer clic en él, pero también puede especificar un valor de tiempo de espera.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementar información sobre herramientas para los iconos de la barra de estado

En el fragmento de código siguiente se muestra cómo agregar una información sobre herramientas de globo a un icono de la barra de estado.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Observaciones

Para obtener una explicación detallada de la barra de estado, consulte [la barra de tareas](/windows/desktop/shell/taskbar).

Para mostrar una información sobre herramientas de globo, debe establecer la \_ marca de información de NSI en la estructura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) y usar los miembros **szInfo** y **uTimeout** para especificar el texto de la información sobre herramientas y la duración del tiempo de espera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 