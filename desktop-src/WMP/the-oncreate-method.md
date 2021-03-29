---
title: Método alcrear
description: Método alcrear
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Complementos de Windows Media Player, método de creación
- complementos, método de creación
- Complementos de la interfaz de usuario, método de creación
- Complementos de la interfaz de usuario, método de creación
- Método alcrear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903157"
---
# <a name="the-oncreate-method"></a>Método alcrear

Se llama al método alcrear cuando se crea por primera vez la ventana del complemento.

El siguiente código se usa para implementar este método:


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



Este método crea el botón **Buscar** y lo asocia al \_ identificador de comando de búsqueda de IDC, que se define al principio del archivo:


```C++
#define IDC_SEARCH 2000

```



Este identificador de comando se asigna al método de búsqueda en la sección mapa de mensajes que se ha descrito anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




