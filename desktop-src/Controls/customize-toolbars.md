---
title: Personalización de las barras de herramientas
description: La mayoría Windows aplicaciones basadas en herramientas usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f098880676fc0404df2a68694dc80b8601c21926d94ff594029321bafb1528a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929555"
---
# <a name="how-to-customize-toolbars"></a>Personalización de las barras de herramientas

La mayoría Windows aplicaciones basadas en herramientas usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa. Sin embargo, las barras de herramientas estáticas tienen algunas deficiencias, como demasiado poco espacio para mostrar eficazmente todas las herramientas disponibles. La solución a este problema es hacer que las barras de herramientas de la aplicación se personalizaciónn por el usuario. A continuación, los usuarios pueden optar por mostrar solo las herramientas que necesitan y organizarlas de forma que se adapten a su estilo de trabajo personal.

> [!Note]  
> Las barras de herramientas de los cuadros de diálogo no se pueden personalizar.

 

Para habilitar la personalización, incluya la marca de estilo de controles comunes [**CCS \_ ADJUSTABLE**](common-control-styles.md) al crear el control de barra de herramientas. Hay dos enfoques básicos para la personalización:

-   Cuadro de diálogo de personalización. Este cuadro de diálogo proporcionado por el sistema es el enfoque más sencillo. Proporciona a los usuarios una interfaz gráfica de usuario que les permite agregar, eliminar o mover iconos.
-   Arrastrar y colocar herramientas. La implementación de la funcionalidad de arrastrar y colocar permite a los usuarios mover herramientas a otra ubicación de la barra de herramientas o eliminarlas arrastrándolas fuera de la barra de herramientas. Proporciona a los usuarios una manera rápida y sencilla de organizar su barra de herramientas, pero no les permite agregar herramientas.

Puede implementar un enfoque o ambos, en función de las necesidades de la aplicación. Ninguno de estos dos enfoques de personalización proporciona un mecanismo integrado, como un botón Cancelar o Deshacer, para devolver la barra de herramientas a su estado anterior. Debe usar explícitamente la API de control de barra de herramientas para almacenar el estado de personalización previa de la barra de herramientas. Si es necesario, puede usar más adelante esta información almacenada para restaurar la barra de herramientas a su estado original.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="customization-dialog-box"></a>Cuadro de diálogo Personalización

El control de barra de herramientas proporciona el cuadro de diálogo de personalización para proporcionar a los usuarios una manera sencilla de agregar, mover o eliminar herramientas. Los usuarios pueden iniciarlo haciendo doble clic en la barra de herramientas. Las aplicaciones pueden iniciar el cuadro de diálogo de personalización mediante programación mediante el envío del control de barra de herramientas de un [**mensaje CUSTOMIZE \_ de TB.**](tb-customize.md)

En la ilustración siguiente se muestra un ejemplo del cuadro de diálogo de personalización de la barra de herramientas.

![captura de pantalla de una ventana con una barra de herramientas de tres elementos y un cuadro de diálogo con listas de los botones de barra de herramientas disponibles y actuales](images/tb-customdlg.png)

Las herramientas del cuadro de lista de la derecha son las que se encuentran actualmente en la barra de herramientas. Inicialmente, esta lista contendrá las herramientas que especifique al crear la barra de herramientas. El cuadro de lista de la izquierda contiene las herramientas que están disponibles para agregar a la barra de herramientas. La aplicación es responsable de rellenar esa lista (que no sea con el separador, que aparece automáticamente).

El control de barra de herramientas notifica a la aplicación que está iniciando un cuadro de diálogo de personalización enviando a su ventana primaria un código de [notificación \_ BEGINADJUST](tbn-beginadjust.md) de TBN seguido de un código de notificación [ \_ INITCUSTOMIZE de TBN.](tbn-initcustomize.md) En la mayoría de los casos, la aplicación no necesita responder a estos códigos de notificación. Sin embargo, si no desea que el cuadro de diálogo Personalizar barra de herramientas muestre un botón Ayuda, controle TBN \_ INITCUSTOMIZE devolviendo TBNRF \_ HIDEHELP.

A continuación, el control de barra de herramientas recopila la información que necesita para inicializar el cuadro de diálogo mediante el envío de tres series de códigos de notificación, en el orden siguiente:

-   Un [código de notificación \_ QUERYINSERT](tbn-queryinsert.md) de TBN para cada botón de la barra de herramientas para determinar dónde se pueden insertar botones. Devuelve **FALSE** para evitar que se inserte un botón a la izquierda del botón especificado en el mensaje de notificación. Si devuelve **FALSE a** todos los códigos de notificación QUERYINSERT de TBN, no se mostrará \_ el cuadro de diálogo.
-   Un [código de notificación \_ QUERYDELETE de TBN](tbn-querydelete.md) para cada herramienta que se encuentra actualmente en la barra de herramientas. Devuelve **TRUE** si se puede eliminar una herramienta o **FALSE** si no es así.
-   Una serie de [códigos de notificación \_ GETBUTTONINFO](tbn-getbuttoninfo.md) de TBN para rellenar la lista de botones disponibles. Para agregar un botón a la lista, rellene la estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que se pasa con el código de notificación y devuelva **TRUE.** Cuando no tenga más herramientas para agregar, devuelva **FALSE.** Tenga en cuenta que puede devolver información para los botones que ya están en la barra de herramientas; estos botones no se agregarán a la lista.

A continuación, se muestra el cuadro de diálogo y el usuario puede empezar a personalizar la barra de herramientas.

Cuando el cuadro de diálogo está abierto, la aplicación puede recibir una variedad de códigos de notificación, en función de las acciones del usuario:

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). El usuario ha cambiado la ubicación de una herramienta en la barra de herramientas o ha agregado una herramienta. Devuelve **FALSE** para evitar que la herramienta se inserte en esa ubicación.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). El usuario está a punto de quitar una herramienta de la barra de herramientas.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). El usuario ha hecho clic en el botón Ayuda.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). El usuario ha agregado, movido o eliminado una herramienta.
-   [TBN \_ RESTABLEZCA](tbn-reset.md). El usuario ha hecho clic en el botón Restablecer.

Una vez que se destruye el cuadro de diálogo, la aplicación recibirá un [código de notificación \_ ENDADJUST de TBN.](tbn-endadjust.md)

En el ejemplo de código siguiente se muestra una manera de implementar la personalización de la barra de herramientas.


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>Herramientas de arrastrar y colocar

Los usuarios también pueden reorganizar los botones de una barra de herramientas presionando la tecla MAYÚS y arrastrando el botón a otra ubicación. El proceso de arrastrar y colocar se controla automáticamente mediante el control de barra de herramientas. Muestra una imagen fantasma del botón a medida que se arrastra y reorganiza la barra de herramientas después de que se ha eliminado. Los usuarios no pueden agregar botones de esta manera, pero pueden eliminar un botón si lo quitan de la barra de herramientas.

Aunque el control de barra de herramientas normalmente realiza esta operación automáticamente, también envía a la aplicación dos códigos de notificación: [TBN \_ QUERYDELETE](tbn-querydelete.md) y [TBN \_ QUERYINSERT](tbn-queryinsert.md). Para controlar el proceso de arrastrar y colocar, controle estos códigos de notificación de la manera siguiente:

-   El [código de notificación \_ QUERYDELETE](tbn-querydelete.md) de TBN se envía en cuanto el usuario intenta mover el botón, antes de que se muestre el botón fantasma. Devuelve **FALSE** para evitar que se mueven los botones. Si devuelve **TRUE**, el usuario podrá mover la herramienta o eliminarla si la quita de la barra de herramientas. Si se puede mover una herramienta, se puede eliminar. Sin embargo, si el usuario elimina una herramienta, el control de barra de herramientas enviará a la aplicación un código de notificación [ \_ TBN DELETINGBUTTON,](tbn-deletingbutton.md) momento en el que puede optar por volver a insertar el botón en su ubicación original, con lo que se cancela la eliminación.
-   El [código de notificación \_ QUERYINSERT](tbn-queryinsert.md) de TBN se envía cuando el usuario intenta colocar el botón en la barra de herramientas. Para evitar que el botón que se mueve se descime a la izquierda del botón especificado en la notificación, devuelva **FALSE**. Este código de notificación no se envía si el usuario quita la herramienta de la barra de herramientas.

Si el usuario intenta arrastrar un botón sin presionar también la tecla MAYÚS, el control de barra de herramientas no controlará la operación de arrastrar y colocar. Sin embargo, enviará a la aplicación un código de notificación [ \_ BEGINDRAG](tbn-begindrag.md) de TBN para indicar el inicio de una operación de arrastre y un código de [notificación \_ ENDDRAG](tbn-enddrag.md) de TBN para indicar el final. Si desea habilitar esta forma de arrastrar y colocar, la aplicación debe controlar estos códigos de notificación, proporcionar la interfaz de usuario necesaria y modificar la barra de herramientas para reflejar los cambios.

### <a name="saving-and-restoring-toolbars"></a>Guardar y restaurar barras de herramientas

En el proceso de personalización de una barra de herramientas, es posible que la aplicación tenga que guardar información para que pueda restaurar la barra de herramientas a su estado original. Para iniciar el guardado o la restauración de un estado de barra de herramientas, envíe al control de barra de herramientas un mensaje [**\_ SAVERESTORE**](tb-saverestore.md) de TB con *lParam* establecido en **TRUE.** El *valor lParam* de este mensaje especifica si está solicitando una operación de guardado o restauración. Una vez enviado el mensaje, hay dos maneras de controlar la operación de guardado y restauración:

-   Con los controles [comunes versión 4.72](common-control-versions.md) y anteriores, debe implementar un controlador [ \_ GETBUTTONINFO de TBN.](tbn-getbuttoninfo.md) El control de barra de herramientas envía este código de notificación para solicitar información sobre cada botón a medida que se restaura.
-   La versión 5.80 incluye una opción de guardar o restaurar. Al principio del proceso, y a medida que se guarde o restaure cada botón, la aplicación recibirá un código de [notificación \_ TBN SAVE](tbn-save.md) o [TBN \_ RESTORE.](tbn-restore.md) Para usar esta opción, debe implementar controladores de notificación para proporcionar la información de mapa de bits y estado necesaria para guardar o restaurar correctamente el estado de la barra de herramientas.

Los estados de la barra de herramientas se guardan en un flujo de datos que consta de bloques de datos definidos por shell que alternan con bloques de datos definidos por la aplicación. Se almacena un bloque de datos de cada tipo para cada botón, junto con un bloque opcional de datos globales que las aplicaciones pueden colocar al principio de la secuencia. Durante el proceso de guardado, el [controlador \_ SAVE de TBN](tbn-save.md) agrega los bloques definidos por la aplicación al flujo de datos. Durante el proceso de restauración, el controlador RESTORE de [TBN \_ ](tbn-restore.md) lee cada bloque y proporciona al shell la información que necesita para reconstruir la barra de herramientas.

### <a name="how-to-handle-a-tbn_save-notification"></a>Cómo controlar una notificación SAVE de TBN \_

El primer [código de notificación \_ SAVE](tbn-save.md) de TBN se envía al principio del proceso de guardado. Antes de guardar los botones, los miembros de la estructura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) se establecen como se muestra en la tabla siguiente.



| Miembro       | Configuración                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Cantidad de memoria necesaria para los datos definidos por Shell.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Número de botones.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Cantidad calculada de memoria necesaria para los datos definidos por la aplicación. Normalmente, se incluyen algunos datos globales, además de datos para cada botón. Agregue ese valor a **cbData** y asigne suficiente memoria **a pData** para contenerlo todo.                                                                                                                      |
| **pCurrent** | Primer byte sin usar en el flujo de datos. Si no necesita información de la barra de herramientas global, establezca **pCurrent** pData para que apunta al  =   inicio del flujo de datos. Si necesita información de la barra de herramientas global, almacénela en **pData** y, a continuación, establezca **pCurrent** al principio de la parte no utilizada del flujo de datos antes de volver. |



 

Si desea agregar información de la barra de herramientas global, pónla al principio del flujo de datos. Avance **pCurrent** hasta el final de los datos globales para que apunta al principio de la parte no utilizada del flujo de datos y devuelva.

Después de volver, el Shell comienza a guardar la información del botón. Agrega los datos definidos por Shell para el primer botón en **pCurrent** y, a continuación, avanza **pCurrent** al principio de la parte no utilizada.

Después de guardar cada botón, se envía un código de [notificación \_ SAVE](tbn-save.md) de TBN y [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) se devuelve con estos miembros establecidos como se muestra a continuación.



| Miembro                       | Configuración                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Índice de base cero del número de botón.                                                                                                                                                                                                                           |
| **pCurrent**                 | Puntero al primer byte sin usar del flujo de datos. Si desea almacenar información adicional sobre el botón, almacénelo en la ubicación a la que apunta **pCurrent** y actualice **pCurrent** para que apunte a la primera parte no utilizada del flujo de datos después de eso. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que describe el botón que se va a guardar.                                                                                                                                                                              |



 

Cuando reciba el código de notificación, debe extraer cualquier información específica del botón que necesite de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). Recuerde que al agregar un botón, puede usar el **miembro dwData** de **TBBUTTON** para contener datos específicos de la aplicación. Cargue los datos en el flujo de datos en **pCurrent**. Avance **pCurrent** hasta el final de los datos, apuntando de nuevo al principio de la parte no utilizada de la secuencia y devuelva .

A continuación, el shell va al botón siguiente, agrega su información a **pData,** avanza **pCurrent,** carga [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y envía otro código de [notificación DE TBN \_ SAVE.](tbn-save.md) Este proceso continúa hasta que se guardan todos los botones.

### <a name="restoring-saved-toolbars"></a>Restaurar barras de herramientas guardadas

Básicamente, el proceso de restauración invierte el proceso de guardado. Al principio, la aplicación recibirá un código de notificación RESTORE de [TBN \_](tbn-restore.md) con el **miembro iItem** de la estructura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) establecido en –1. El **miembro cbData** se establece en el tamaño de **pData** y **cButtons** se establece en el número de botones.

El controlador de notificaciones debe extraer la información global que se colocó al principio de **pData** durante el guardado y avanzar **pCurrent** al principio del primer bloque de datos definidos por Shell. Establezca **cBytesPerRecord en** el tamaño de los bloques de datos que usó para guardar los datos del botón. Establezca **cButtons en** el número de botones y vuelva.

El siguiente [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) es para el primer botón. El **miembro pCurrent** apunta al inicio del primer bloque de datos de botón e **iItem** se establece en el índice del botón. Extraiga los datos y avance **pCurrent**. Cargue los datos en [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y vuelva. Para omitir un botón de la barra de herramientas restaurada, establezca el **miembro idCommand** de **TBBUTTON** en cero. El shell repetirá el proceso de los botones restantes. Además de los mensajes [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) y **NMTBRESTORE,** también puede usar mensajes como [TBN \_ RESET](tbn-reset.md) para guardar y restaurar una barra de herramientas.

En el ejemplo de código siguiente se guarda una barra de herramientas antes de personalizarla y se restaura si la aplicación recibe un [mensaje DE RESTABLECIMIENTO \_ DE TBN.](tbn-reset.md)


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[**Valores de índice de imagen del botón Estándar de la barra de herramientas**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




