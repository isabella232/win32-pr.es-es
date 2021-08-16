---
title: Buscar y reemplazar cuadros de diálogo
description: Muestra un cuadro de diálogo no modelo que permite al usuario especificar una cadena que se buscará, así como las opciones que se usarán al buscar texto en un documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows Interfaz de usuario,entrada del usuario
- Windows Interfaz de usuario,Common Dialog Box Library
- entrada de usuario, Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Buscar, cuadro de diálogo
- Reemplazar (cuadro de diálogo)
- personalizar el cuadro de diálogo Buscar
- personalizar el cuadro de diálogo Reemplazar
- cuadros de diálogo predefinidos
- cuadros de diálogo, Buscar
- cuadros de diálogo, Reemplazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59bc5da5a8780a4f08bbf4bf757e1703d8d9120fdefe9d1730e515ffc6feae40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503497"
---
# <a name="find-and-replace-dialog-boxes"></a>Buscar y reemplazar cuadros de diálogo

Muestra un cuadro de diálogo no modelo que permite al usuario especificar una cadena que se buscará, así como las opciones que se usarán al buscar texto en un documento. El **cuadro** de diálogo Reemplazar permite al usuario especificar una cadena para buscar y una cadena de reemplazo, así como opciones para controlar la operación.

Para crear y mostrar un **cuadro de diálogo Buscar,** inicialice una [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y pase la estructura a la [**función FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) En la ilustración siguiente se muestra un cuadro **de diálogo Buscar** típico.

![cuadro de diálogo buscar](images/finddialogboxxp.png)

Para crear y mostrar un **cuadro de diálogo Reemplazar,** inicialice una [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y pase la estructura a la [**función ReplaceText.**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) En la ilustración siguiente se muestra un cuadro **de diálogo Reemplazar** típico.

![reemplazar cuadro de diálogo](images/replacedialogboxxp.png)

A diferencia de otros cuadros de diálogo comunes, **los** cuadros de **diálogo** Buscar y Reemplazar son modelados. Un cuadro de diálogo no modelo permite al usuario cambiar entre el cuadro de diálogo y la ventana que lo creó. Esto es útil para permitir que el usuario busque una cadena, cambie a la ventana de la aplicación para trabajar en la cadena y vuelva al cuadro de diálogo para buscar otra cadena sin repetir el comando necesario para abrir el cuadro de diálogo.

Si la [**función FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) [**o ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) crea correctamente el cuadro de diálogo, devuelve un identificador al cuadro de diálogo. Puede usar este identificador para moverse y comunicarse con el cuadro de diálogo. Si la función no puede crear el cuadro de diálogo, devuelve **NULL.** Puede determinar la causa de un error llamando a la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se tratan los temas siguientes.

-   [Mensaje registrado de FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalizar el cuadro de diálogo Buscar o reemplazar](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Mensaje registrado de FINDMSGSTRING

Antes de crear **un cuadro de** diálogo Buscar o reemplazar, debe llamar a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje para el [**mensaje registrado FINDMSGSTRING.**](findmsgstring.md)  A continuación, puede usar el identificador para detectar y procesar los mensajes enviados desde el cuadro de diálogo. Cuando el usuario hace clic en  los botones Buscar **siguiente,** Reemplazar o Reemplazar todo en un cuadro de diálogo, el procedimiento del cuadro de diálogo envía un mensaje **FINDMSGSTRING** al procedimiento de ventana de la ventana propietaria. Al crear el cuadro de diálogo, el **miembro hwndOwner** de la [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica la ventana de propietario.

El *parámetro lParam* de un [**mensaje FINDMSGSTRING**](findmsgstring.md) es un puntero a la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que especificó al crear el cuadro de diálogo. Antes de enviar el mensaje, el cuadro de diálogo establece los miembros de esta estructura con la entrada de usuario más reciente, incluida la cadena que se va a buscar, la cadena de reemplazo (si la hay) y las opciones para la operación de búsqueda y reemplazo.

En un [**mensaje FINDMSGSTRING,**](findmsgstring.md) el miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) incluye una de las marcas siguientes para indicar el evento que provocó el mensaje.



| Marca               | Significado                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | El cuadro de diálogo se está cerrando. Una vez que la ventana de propietario procesa este mensaje, un identificador del cuadro de diálogo ya no es válido.                                                                                    |
| **FR \_ FINDNEXT**   | El usuario hizo clic en **el botón Buscar** siguiente en un cuadro **de** **diálogo** Buscar o reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a buscar.                                                         |
| **FR \_ REPLACE**    | El usuario hizo clic en **el botón Reemplazar** en un cuadro de **diálogo** Reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a reemplazar y el **miembro lpstrReplaceWith** especifica la cadena de reemplazo.     |
| **FR \_ REPLACEALL** | El usuario hizo clic en **el botón Reemplazar** todo en un cuadro de **diálogo** Reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a reemplazar y el **miembro lpstrReplaceWith** especifica la cadena de reemplazo. |



 

Para un **mensaje Buscar siguiente** **o** Reemplazar todo, el **miembro Flags** puede incluir cualquier combinación de las marcas siguientes para indicar las opciones de búsqueda.



| Marca              | Significado                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN**      | Si se establece, se selecciona **el** botón Abajo de los botones de radio de dirección, lo que indica que el usuario desea buscar desde la ubicación actual hasta el final del documento. Si **FR \_ DOWN** no está establecido, **se** selecciona el botón Arriba para que el usuario quiera buscar al principio del documento.       |
| **FR \_ MATCHCASE** | Si se establece, se **selecciona la casilla Coincidir** mayúsculas y minúsculas, lo que indica que el usuario quiere que la búsqueda tenga en cuenta las mayúsculas y minúsculas. Si **FR \_ MATCHCASE** no está establecido, la casilla no está seleccionada para que la búsqueda no tenga en cuenta mayúsculas de minúsculas.                                                                       |
| **FR \_ WHOLEWORD** | Si se establece, la **casilla** Coincidir solo palabra entera está activada, lo que indica que el usuario desea buscar solo palabras enteras que coincidan con la cadena de búsqueda. Si **FR \_ WHOLEWORD** no está establecido, la casilla no está seleccionada, por lo que también debe buscar fragmentos de palabras que coincidan con la cadena de búsqueda. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalizar el cuadro de diálogo Buscar o reemplazar

Para personalizar un **cuadro de** **diálogo** Buscar o reemplazar, puede usar cualquiera de los métodos siguientes:

-   Especificar valores en la [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) al crear el cuadro de diálogo
-   Proporcionar una plantilla personalizada
-   Proporcionar un procedimiento de enlace

Al crear un  **cuadro** de diálogo Buscar o reemplazar, puede establecer marcas en el miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para ocultar o deshabilitar cualquiera de los controles de opción de búsqueda. Por ejemplo, puede establecer la marca FR NOMATCHCASE para deshabilitar la casilla Caso de coincidencia o establecer la marca \_ FR  \_ HIDEMATCHCASE para ocultarla.

Puede proporcionar una plantilla  personalizada  para un cuadro de diálogo Buscar o reemplazar, por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. Las [**funciones FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) [**y ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usan la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para un cuadro de diálogo Buscar o reemplazar**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Findtext.dlg. Los identificadores de control usados en la plantilla **de** cuadro de diálogo Buscar **o** Reemplazar predeterminada se definen en el archivo Dlgs.h.
2.  Use la [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para habilitar la plantilla de la siguiente manera:
    -   -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca FR \_ ENABLETEMPLATE en el **miembro Flags.** Use los **miembros hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso.

            -O bien-

        -   Si la plantilla personalizada ya está en memoria, establezca la \_ marca FR ENABLETEMPLATEHANDLE. Use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento [**de enlace FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) para un **cuadro de** **diálogo** Buscar o reemplazar. El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada de los controles.

**Para habilitar un procedimiento de enlace para un cuadro de diálogo Buscar o reemplazar**

1.  Establezca la marca \_ FR ENABLEHOOK en el **miembro Flags** de la [**estructura FINDREPLACE.**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnHook.**

Después de procesar [**su mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el procedimiento del cuadro de diálogo envía un mensaje **WM \_ INITDIALOG** al procedimiento de enlace. El *parámetro lParam* de este mensaje es un puntero a la [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) utilizada para inicializar el cuadro de diálogo.

Si el procedimiento de enlace devuelve **FALSE** en respuesta al mensaje [**WM \_ INITDIALOG,**](wm-initdialog.md) el cuadro de diálogo no se mostrará a menos que el procedimiento de enlace lo muestre. Para ello, realice primero cualquier otra operación de pintura y, a continuación, llame a [**las funciones ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) [**y UpdateWindow.**](/windows/desktop/api/winuser/nf-winuser-updatewindow) El siguiente fragmento de código muestra un ejemplo:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 