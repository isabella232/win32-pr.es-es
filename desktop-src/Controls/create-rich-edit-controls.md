---
title: Cómo crear controles Rich Edit
description: Para crear un control Rich Edit, llame a la función CreateWindowEx y especifique la clase Rich Edit Window.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078420"
---
# <a name="how-to-create-rich-edit-controls"></a>Cómo crear controles Rich Edit

Para crear un control Rich Edit, llame a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase Rich Edit Window. Para Microsoft Rich Edit 4,1 (Msftedit.dll), especifique \_ la clase MSFTEDIT como clase de ventana. En todas las versiones anteriores, especifique la \_ clase RICHEDIT. Para obtener más información, vea [versiones de Rich Edit](about-rich-edit-controls.md).

Los controles Rich Edit admiten la mayoría de los estilos de ventana que se usan con los controles de edición, así como estilos adicionales. Debe especificar el estilo de ventana de [**\_ varias líneas Multiline**](edit-control-styles.md) si desea permitir más de una línea de texto en el control. Para obtener más información, vea [estilos de control Rich Edit](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="create-a-rich-edit-control"></a>Crear un control Rich Edit

En la función de ejemplo siguiente se crea un control Rich Edit y se inicializa con texto.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



En Microsoft Visual Studio 2005 y versiones posteriores, es posible agregar un control Rich Edit en una plantilla de cuadro de diálogo arrastrando el control desde el cuadro de herramientas. Sin embargo, si lo hace en el editor de cuadros de diálogo, no se asegura de que se cargue la biblioteca necesaria antes de crear el control. Es necesario llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Riched32.dll, Riched20.dll o Msftedit.dll antes de que se cree el cuadro de diálogo.

## <a name="remarks"></a>Observaciones

Para usar estilos visuales con estos controles, una aplicación debe incluir un manifiesto y debe llamar a la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 