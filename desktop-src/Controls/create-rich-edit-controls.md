---
title: Cómo crear controles rich edit
description: Para crear un control de edición enriquecido, llame a la función CreateWindowEx y especifique la clase de ventana de edición enriquecida.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7972282f02bb5ba6edc202ce1f2888dee48d7f8ae488a324cd7298a8e70ba0d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826395"
---
# <a name="how-to-create-rich-edit-controls"></a>Cómo crear controles rich edit

Para crear un control de edición enriquecido, llame a [**la función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de edición enriquecida. Para Microsoft Rich Edit 4.1 (Msftedit.dll), especifique MSFTEDIT \_ CLASS como clase de ventana. Para todas las versiones anteriores, especifique RICHEDIT \_ CLASS. Para obtener más información, vea [Versions of Rich Edit](about-rich-edit-controls.md).

Los controles de edición enriquecciones admiten la mayoría de los estilos de ventana usados con controles de edición, así como estilos adicionales. Debe especificar el estilo [**de ventana ES \_ MULTILINE**](edit-control-styles.md) si desea permitir más de una línea de texto en el control . Para obtener más información, vea [Rich Edit Control Styles](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-rich-edit-control"></a>Crear un control Rich Edit

En la siguiente función de ejemplo se crea un control de edición enriquecido y se inicializa con texto.


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



En Microsoft Visual Studio 2005 y versiones posteriores, es posible agregar un control de edición enriquecido a una plantilla de cuadro de diálogo arrastrando el control desde el cuadro de herramientas. Sin embargo, esto en el editor de cuadros de diálogo no garantiza que la biblioteca necesaria se cargará antes de crear el control. Es necesario llamar a la [**función LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Riched32.dll, Riched20.dll o Msftedit.dll antes de crear el cuadro de diálogo.

## <a name="remarks"></a>Comentarios

Para usar estilos visuales con estos controles, una aplicación debe incluir un manifiesto y debe llamar a la [**función InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [Estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 