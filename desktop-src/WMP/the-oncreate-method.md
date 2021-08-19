---
title: El método OnCreate
description: El método OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Reproductor de Windows Media complementos, método OnCreate
- plug-ins,OnCreate (método)
- complementos de interfaz de usuario, método OnCreate
- Complementos de interfaz de usuario, método OnCreate
- Método OnCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac52b1c58c6799f89d29fb1ee24c09767fee26729e760b2b454f1a359bd57596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118113"
---
# <a name="the-oncreate-method"></a>El método OnCreate

Se llama al método OnCreate cuando se crea por primera vez la ventana del complemento.

El código siguiente se usa para implementar este método:


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

 

 




