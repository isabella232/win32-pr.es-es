---
title: Uso de Hot-Tracking con barras de herramientas
description: Cuando un puntero del mouse mantiene el puntero sobre un elemento, el elemento se activa. Si está habilitado el seguimiento en caliente, el elemento de acceso activa se resalta. Una barra de herramientas que se crea con el estilo TBSTYLE FLAT, o una que usa estilos visuales, admite el seguimiento en caliente \_ de forma predeterminada.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829095"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Uso de Hot-Tracking con barras de herramientas

Cuando un puntero del mouse mantiene el puntero sobre un elemento, el elemento se activa. Si está habilitado el seguimiento en caliente, el elemento de acceso activa se resalta. Una barra de herramientas que se crea con el estilo [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o una que usa estilos visuales [admite](themes-overview.md)el seguimiento rápido de forma predeterminada.

El seguimiento en caliente requiere que cree listas de imágenes. Por lo tanto, no puede usar el mensaje [**\_ ADDBITMAP de TB**](tb-addbitmap.md) o la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para crear la barra de herramientas.

Cuando el mouse mantiene el mouse sobre un botón de la barra de herramientas, el botón se describe para resaltarlo. En la ilustración siguiente se muestra una barra de herramientas con el seguimiento rápido habilitado; el puntero del mouse se desplazaba sobre el botón Guardar cuando se tomó la captura de pantalla.

![captura de pantalla de un cuadro de diálogo con una barra de herramientas de tres elementos; se describe el icono seleccionado](images/tb-withstyles.png)

Si desea que un mapa de bits de botón de la barra de herramientas cambie cuando cambie el estado del control, almacene las distintas imágenes en las [listas de imágenes](image-lists.md). Por ejemplo, algunas aplicaciones tienen botones de barra de herramientas en blanco y negro que se coloreados cuando se seleccionan. Las dos imágenes diferentes se almacenan en listas de imágenes. Las barras de herramientas admiten el uso de hasta tres listas de imágenes. Normalmente, una aplicación tiene una lista predeterminada, deshabilitada y de seguimiento en caliente de imágenes. Para establecer y recuperar listas de imágenes para los botones de la barra de herramientas activa, use los mensajes [**\_ TB SETHOTIMAGELIST**](tb-sethotimagelist.md) y [**TB \_ GETHOTIMAGELIST.**](tb-gethotimagelist.md)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-hot-tracking-with-a-toolbar"></a>Usar Hot-Tracking con una barra de herramientas

En el ejemplo de código siguiente se crea, rellena y asigna una lista de imágenes para los botones de acceso rápido.


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

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




