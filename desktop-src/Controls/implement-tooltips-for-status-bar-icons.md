---
title: Cómo implementar información sobre herramientas para iconos de barra de estado
description: Una manera no intrusiva de mostrar un mensaje explicativo para un icono de barra de estado es implementar una información sobre herramientas. La información sobre herramientas desaparece cuando se hace clic en ella, pero también se puede especificar un valor de tiempo de espera.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958589"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Cómo implementar información sobre herramientas para iconos de barra de estado

Una manera no intrusiva de mostrar un mensaje explicativo para un icono de barra de estado es implementar una información sobre herramientas. La información sobre herramientas desaparece cuando se hace clic en ella, pero también se puede especificar un valor de tiempo de espera.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementar información sobre herramientas para iconos de barra de estado

En el fragmento de código siguiente se muestra cómo agregar información sobre herramientas de globo a un icono de barra de estado.


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



## <a name="remarks"></a>Comentarios

Para obtener una explicación detallada de la barra de estado, vea [La barra de tareas](/windows/desktop/shell/taskbar).

Para mostrar una información sobre herramientas de globo, debe establecer la marca DE INFORMACIÓN DE NIF en la estructura NOTIFYICONDATA y usar los miembros \_ **szInfo** y **uTimeout** para especificar el texto de la información sobre herramientas y la duración del tiempo de espera. [](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 