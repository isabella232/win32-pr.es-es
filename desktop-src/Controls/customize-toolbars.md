---
title: Cómo personalizar las barras de herramientas
description: La mayoría de las aplicaciones basadas en Windows usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104077468"
---
# <a name="how-to-customize-toolbars"></a>Cómo personalizar las barras de herramientas

La mayoría de las aplicaciones basadas en Windows usan controles de barra de herramientas para proporcionar a los usuarios un acceso cómodo a la funcionalidad del programa. Sin embargo, las barras de herramientas estáticas tienen algunas deficiencias, como un poco de espacio para mostrar eficazmente todas las herramientas disponibles. La solución a este problema consiste en hacer que las barras de herramientas de la aplicación sean personalizables por el usuario. A continuación, los usuarios pueden elegir mostrar solo las herramientas que necesitan y pueden organizarlas de forma que se adapten a su estilo de estilo personal.

> [!Note]  
> Las barras de herramientas de los cuadros de diálogo no se pueden personalizar.

 

Para habilitar la personalización, incluya la marca de estilo de los controles comunes de [**CCS \_ ajustable**](common-control-styles.md) al crear el control de barra de herramientas. Hay dos enfoques básicos para la personalización:

-   Cuadro de diálogo de personalización. Este cuadro de diálogo proporcionado por el sistema es el enfoque más sencillo. Ofrece a los usuarios una interfaz gráfica de usuario que les permite agregar, eliminar o mover iconos.
-   Arrastrar y colocar herramientas. La implementación de la funcionalidad de arrastrar y colocar permite a los usuarios mover herramientas a otra ubicación de la barra de herramientas o eliminarlas arrastrándolas fuera de la barra de herramientas. Proporciona a los usuarios una manera rápida y sencilla de organizar su barra de herramientas, pero no les permite agregar herramientas.

Puede implementar cualquier enfoque o ambos, en función de las necesidades de la aplicación. Ninguno de estos dos enfoques para la personalización proporciona un mecanismo integrado, como un botón Cancelar o deshacer, para devolver la barra de herramientas a su estado anterior. Debe utilizar explícitamente la API de control de barra de herramientas para almacenar el estado de prepersonalización de la barra de herramientas. Si es necesario, puede utilizar posteriormente esta información almacenada para restaurar la barra de herramientas a su estado original.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="customization-dialog-box"></a>Cuadro de diálogo Personalización

El cuadro de diálogo de personalización lo proporciona el control de barra de herramientas para proporcionar a los usuarios una manera sencilla de agregar, quitar o eliminar herramientas. Los usuarios pueden iniciarlo haciendo doble clic en la barra de herramientas. Las aplicaciones pueden iniciar el cuadro de diálogo de personalización mediante programación enviando el control de barra de herramientas a un mensaje de [**\_ Personalización de TB**](tb-customize.md) .

En la ilustración siguiente se muestra un ejemplo del cuadro de diálogo de personalización de la barra de herramientas.

![captura de pantalla de una ventana con una barra de herramientas de tres elementos y un cuadro de diálogo con listas de los botones de la barra de herramientas disponibles y actuales](images/tb-customdlg.png)

Las herramientas del cuadro de lista de la derecha son las que están actualmente en la barra de herramientas. Inicialmente, esta lista contendrá las herramientas que se especifican al crear la barra de herramientas. El cuadro de lista de la izquierda contiene las herramientas que están disponibles para agregarse a la barra de herramientas. La aplicación es responsable de rellenar esa lista (excepto con el separador, que aparece automáticamente).

El control de barra de herramientas notifica a la aplicación que está iniciando un cuadro de diálogo de personalización mediante el envío de su ventana primaria a un código de notificación [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguido de un código de notificación [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) . En la mayoría de los casos, la aplicación no necesita responder a estos códigos de notificación. Sin embargo, si no desea que el cuadro de diálogo Personalizar barra de herramientas muestre un botón ayuda, controle TBN \_ INITCUSTOMIZE devolviendo TBNRF \_ HIDEHELP.

A continuación, el control de barra de herramientas recopila la información que necesita para inicializar el cuadro de diálogo mediante el envío de tres series de códigos de notificación, en el siguiente orden:

-   Un código de notificación de [TBN \_ QUERYINSERT](tbn-queryinsert.md) para cada botón de la barra de herramientas para determinar dónde se pueden insertar los botones. Devuelve **false** para evitar que un botón se inserte a la izquierda del botón especificado en el mensaje de notificación. Si devuelve **false** a todos los códigos de notificación de TBN \_ QUERYINSERT, no se mostrará el cuadro de diálogo.
-   Un código de notificación de [TBN \_ QUERYDELETE](tbn-querydelete.md) para cada herramienta que se encuentra actualmente en la barra de herramientas. Devuelve **true** si se puede eliminar una herramienta o **false** en caso contrario.
-   Una serie de códigos de notificación de [ \_ GETBUTTONINFO de TBN](tbn-getbuttoninfo.md) para rellenar la lista de botones disponibles. Para agregar un botón a la lista, rellene la estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que se pasa con el código de notificación y devuelva **true**. Si no tiene más herramientas para agregar, devuelva **false**. Tenga en cuenta que puede devolver información de los botones que ya están en la barra de herramientas; Estos botones no se agregarán a la lista.

A continuación, se muestra el cuadro de diálogo y el usuario puede empezar a personalizar la barra de herramientas.

Cuando el cuadro de diálogo está abierto, la aplicación puede recibir diversos códigos de notificación, en función de las acciones del usuario:

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). El usuario ha cambiado la ubicación de una herramienta en la barra de herramientas o ha agregado una herramienta. Devuelve **false** para evitar que la herramienta se inserte en esa ubicación.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). El usuario está a punto de quitar una herramienta de la barra de herramientas.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). El usuario hizo clic en el botón ayuda.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). El usuario ha agregado, cambiado o eliminado una herramienta.
-   [TBN \_ RESTABLECER](tbn-reset.md). El usuario hizo clic en el botón Restablecer.

Una vez destruido el cuadro de diálogo, la aplicación recibirá un código de notificación [TBN \_ ENDADJUST](tbn-endadjust.md) .

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



### <a name="dragging-and-dropping-tools"></a>Arrastrar y colocar herramientas

Los usuarios también pueden reorganizar los botones de una barra de herramientas presionando la tecla Mayús y arrastrando el botón hasta otra ubicación. El proceso de arrastrar y colocar se controla automáticamente mediante el control de barra de herramientas. Muestra una imagen fantasma del botón mientras se arrastra y reorganiza la barra de herramientas después de quitarla. Los usuarios no pueden agregar botones de esta manera, pero pueden eliminar un botón colocándolo fuera de la barra de herramientas.

Aunque el control de barra de herramientas realiza normalmente esta operación automáticamente, también envía la aplicación dos códigos de notificación: [TBN \_ QUERYDELETE](tbn-querydelete.md) y [TBN \_ QUERYINSERT](tbn-queryinsert.md). Para controlar el proceso de arrastrar y colocar, controle estos códigos de notificación de la siguiente manera:

-   El código de notificación [TBN \_ QUERYDELETE](tbn-querydelete.md) se envía tan pronto como el usuario intenta quitar el botón, antes de que se muestre el botón fantasma. Devuelve **false** para evitar que el botón se mueva. Si devuelve **true**, el usuario podrá quitar la herramienta o eliminarla colocándolo fuera de la barra de herramientas. Si se puede moverse una herramienta, puede eliminarse. Sin embargo, si el usuario elimina una herramienta, el control de barra de herramientas enviará a la aplicación un código de notificación [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) , momento en el cual podrá optar por volver a insertar el botón en su ubicación original, con lo que se cancelará la eliminación.
-   El código de notificación [ \_ QUERYINSERT de TBN](tbn-queryinsert.md) se envía cuando el usuario intenta quitar el botón de la barra de herramientas. Para evitar que el botón que se está moviendo a la izquierda del botón especificado en la notificación, devuelva **false**. Este código de notificación no se envía si el usuario quita la herramienta de la barra de herramientas.

Si el usuario intenta arrastrar un botón sin presionar también la tecla Mayús, el control de barra de herramientas no controlará la operación de arrastrar y colocar. Sin embargo, enviará a la aplicación un código de notificación [TBN \_ BEGINDRAG](tbn-begindrag.md) para indicar el inicio de una operación de arrastre y un código de notificación de [TBN \_ ENDDRAG](tbn-enddrag.md) para indicar el final. Si desea habilitar esta forma de arrastrar y colocar, la aplicación debe controlar estos códigos de notificación, proporcionar la interfaz de usuario necesaria y modificar la barra de herramientas para reflejar los cambios.

### <a name="saving-and-restoring-toolbars"></a>Guardar y restaurar barras de herramientas

En el proceso de personalización de una barra de herramientas, es posible que la aplicación tenga que guardar la información para que pueda restaurar la barra de herramientas a su estado original. Para iniciar el guardado o la restauración de un estado de la barra de herramientas, envíe el control de barra de herramientas a un mensaje de [**TB \_ SAVERESTORE**](tb-saverestore.md) con el valor de *lParam* establecido en **true**. El valor *lParam* de este mensaje especifica si se solicita una operación de guardar o de restauración. Una vez enviado el mensaje, hay dos formas de controlar la operación de guardar y restaurar:

-   Con los controles comunes [versión 4,72](common-control-versions.md) y versiones anteriores, debe implementar un controlador de [ \_ GETBUTTONINFO de TBN](tbn-getbuttoninfo.md) . El control de barra de herramientas envía este código de notificación para solicitar información sobre cada botón a medida que se restaura.
-   La versión 5,80 incluye una opción guardar/restaurar. Al principio del proceso y, a medida que se guarda o se restaura cada botón, la aplicación recibirá un código de notificación [TBN \_ Save](tbn-save.md) o [TBN \_ restore](tbn-restore.md) . Para usar esta opción, debe implementar controladores de notificación para proporcionar el mapa de bits y la información de estado necesaria para guardar o restaurar correctamente el estado de la barra de herramientas.

Los Estados de la barra de herramientas se guardan en un flujo de datos que consta de bloques de datos definidos por el shell que alternan con bloques de datos definidos por la aplicación. Un bloque de datos de cada tipo se almacena para cada botón, junto con un bloque opcional de datos globales que las aplicaciones pueden colocar al principio de la secuencia. Durante el proceso de almacenamiento, el controlador de [ \_ guardado de TBN](tbn-save.md) agrega los bloques definidos por la aplicación al flujo de datos. Durante el proceso de restauración, el controlador de [ \_ restauración TBN](tbn-restore.md) Lee cada bloque y proporciona al shell la información que necesita para reconstruir la barra de herramientas.

### <a name="how-to-handle-a-tbn_save-notification"></a>Cómo controlar una notificación de \_ guardado de TBN

El primer código de notificación de [ \_ guardar de TBN](tbn-save.md) se envía al principio del proceso de guardar. Antes de guardar cualquier botón, los miembros de la estructura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) se establecen como se muestra en la tabla siguiente.



| Miembro       | Configuración                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Cantidad de memoria necesaria para los datos definidos por el shell.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Número de botones.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Cantidad calculada de memoria necesaria para los datos definidos por la aplicación. Normalmente, se incluyen algunos datos globales, además de los datos de cada botón. Agregue ese valor a **cbData** y asigne suficiente memoria a **pdata** para mantenerlo todo.                                                                                                                      |
| **pCurrent** | Primer byte no utilizado en el flujo de datos. Si no necesita información de la barra de herramientas global, establezca **pCurrent**  =  **pdata** para que apunte al inicio del flujo de datos. Si requiere información de la barra de herramientas global, almacénela en **pdata** y, a continuación, establezca **pCurrent** en el principio de la parte sin usar del flujo de datos antes de volver. |



 

Si desea agregar información de la barra de herramientas global, colóquela al principio del flujo de datos. Avance **pCurrent** hasta el final de los datos globales para que apunte al principio de la parte sin usar del flujo de datos y devuelva.

Después de devolver, el shell comienza a guardar la información del botón. Agrega los datos definidos por el shell para el primer botón en **pCurrent** y, a continuación, avanza **pCurrent** al principio de la parte no utilizada.

Después de guardar cada botón, se envía un código de notificación [TBN \_ Guardar](tbn-save.md) y se devuelve [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) con estos miembros establecidos como se indica a continuación.



| Miembro                       | Configuración                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Índice de base cero del número de botón.                                                                                                                                                                                                                           |
| **pCurrent**                 | Puntero al primer byte no utilizado en el flujo de datos. Si desea almacenar información adicional sobre el botón, almacénelo en la ubicación a la que señala **pCurrent** y actualice **pCurrent** para que apunte a la primera parte sin usar del flujo de datos después. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que describe el botón que se va a guardar.                                                                                                                                                                              |



 

Cuando reciba el código de notificación, debe extraer cualquier información específica del botón que necesite de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). Recuerde que al agregar un botón, puede usar el miembro **dwData** de **TBBUTTON** para almacenar los datos específicos de la aplicación. Cargue los datos en el flujo de datos en **pCurrent**. Avance **pCurrent** hasta el final de los datos, señalando de nuevo al principio de la parte no utilizada del flujo y devuelva.

A continuación, el shell va al botón siguiente, agrega su información a **pdata**, avanza **PCurrent**, carga [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y envía otro código de notificación [TBN \_ Guardar](tbn-save.md) . Este proceso continúa hasta que se guardan todos los botones.

### <a name="restoring-saved-toolbars"></a>Restaurar barras de herramientas guardadas

Básicamente, el proceso de restauración invierte el proceso de guardar. Al principio, la aplicación recibirá un código de notificación [TBN \_ restore](tbn-restore.md) con el miembro **IItem** de la estructura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) establecido en – 1. El miembro **cbData** se establece en el tamaño de **pdata** y **cButtons** se establece en el número de botones.

El controlador de notificación debe extraer la información global que se colocó al principio de **pdata** durante el guardado y avanzar **pCurrent** al principio del primer bloque de datos definidos por el shell. Establezca **cBytesPerRecord** en el tamaño de los bloques de datos que usó para guardar los datos del botón. Establezca **cButtons** en el número de botones y devuelva.

El siguiente [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) es para el primer botón. El miembro **pCurrent** apunta al principio del primer bloque de datos del botón y **iItem** se establece en el índice del botón. Extraiga los datos y avance **pCurrent**. Cargue los datos en [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)y devuelva. Para omitir un botón de la barra de herramientas restaurada, establezca el miembro **idCommand** de **TBBUTTON** en cero. El shell repetirá el proceso para los botones restantes. Además de los mensajes [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) y **NMTBRESTORE** , también puede usar mensajes como [TBN \_ RESET](tbn-reset.md) para guardar y restaurar una barra de herramientas.

En el ejemplo de código siguiente se guarda una barra de herramientas antes de personalizarla y se restaura si la aplicación recibe un mensaje de [ \_ restablecimiento de TBN](tbn-reset.md) .


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

[Usar controles Toolbar](using-toolbar-controls.md)
</dt> <dt>

[**Valores de índice de imagen de botón estándar de la barra de herramientas**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




