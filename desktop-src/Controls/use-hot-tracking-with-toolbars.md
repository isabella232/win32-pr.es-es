---
title: Cómo usar Hot-Tracking con barras de herramientas
description: Cuando se mantiene el puntero del mouse sobre un elemento, el elemento pasa a estar activo. Si está habilitado el seguimiento activo, se resalta el elemento activo. Una barra de herramientas que se crea con el \_ estilo plano TBSTYLE, o una que usa estilos visuales, admite el seguimiento activo de forma predeterminada.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104077470"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Cómo usar Hot-Tracking con barras de herramientas

Cuando se mantiene el puntero del mouse sobre un elemento, el elemento pasa a estar activo. Si está habilitado el seguimiento activo, se resalta el elemento activo. Una barra de herramientas que se crea con el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) , o una que usa [estilos visuales](themes-overview.md), admite el seguimiento activo de forma predeterminada.

El seguimiento activo requiere la creación de listas de imágenes. por lo tanto, no puede usar el mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) o la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para crear la barra de herramientas.

Cuando el mouse se desplaza sobre un botón de la barra de herramientas, el botón se describe para resaltarlo. En la ilustración siguiente se muestra una barra de herramientas con el seguimiento activo habilitado; se mantiene el puntero del mouse en el botón Guardar cuando se tomó la captura de pantalla.

![captura de pantalla de un cuadro de diálogo con una barra de herramientas de tres elementos; se describe el icono seleccionado](images/tb-withstyles.png)

Si desea que un mapa de bits del botón de la barra de herramientas cambie cuando cambie el estado del control, almacene las distintas imágenes en [las listas de imágenes](image-lists.md). Por ejemplo, algunas aplicaciones tienen botones de barra de herramientas en blanco y negro que se colorean cuando se seleccionan. Las dos imágenes diferentes se almacenan en las listas de imágenes. Las barras de herramientas admiten el uso de hasta tres listas de imágenes. Normalmente, una aplicación tiene una lista de imágenes predeterminada, deshabilitada y de seguimiento activo. Para establecer y recuperar listas de imágenes para botones de la barra de herramientas activa, use los mensajes [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) y [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-hot-tracking-with-a-toolbar"></a>Usar Hot-Tracking con una barra de herramientas

En el ejemplo de código siguiente se crea, se rellena y se asigna una lista de imágenes para los botones de acceso rápido.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




