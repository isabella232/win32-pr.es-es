---
title: El método OnCreate
description: El método OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Reproductor de Windows Media complementos,método OnCreate
- complementos, método OnCreate
- complementos de interfaz de usuario, método OnCreate
- Complementos de interfaz de usuario, método OnCreate
- Método OnCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170554"
---
# <a name="the-oncreate-method"></a>El método OnCreate

Se llama al método OnCreate cuando se crea por primera vez la ventana del complemento.

Para implementar este método se usa el código siguiente:


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



Este método crea el **botón Buscar** y lo asocia al identificador del comando SEARCH de IDC, que se define al principio \_ del archivo:


```C++
#define IDC_SEARCH 2000

```



Este identificador de comando se asigna al método OnSearch en la sección de asignación de mensajes descrita anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




