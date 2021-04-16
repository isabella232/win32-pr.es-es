---
title: Cuadros de diálogo Buscar y reemplazar
description: Muestra un cuadro de diálogo no modal que permite al usuario especificar una cadena para buscar, así como las opciones que se pueden usar al buscar texto en un documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, biblioteca de cuadros de diálogo comunes
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Buscar, cuadro de diálogo
- Reemplazar (cuadro de diálogo)
- personalizar buscar (cuadro de diálogo)
- personalizar el cuadro de diálogo reemplazar
- cuadros de diálogo predefinidos
- cuadros de diálogo, buscar
- cuadros de diálogo, reemplazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104563396"
---
# <a name="find-and-replace-dialog-boxes"></a>Cuadros de diálogo Buscar y reemplazar

Muestra un cuadro de diálogo no modal que permite al usuario especificar una cadena para buscar, así como las opciones que se pueden usar al buscar texto en un documento. El cuadro de diálogo **reemplazar** permite al usuario especificar una cadena para buscar y una cadena de reemplazo, así como opciones para controlar la operación.

Puede crear y mostrar un cuadro de diálogo **Buscar** inicializando una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y pasando la estructura a la función [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . En la ilustración siguiente se muestra un cuadro de diálogo de **búsqueda** típico.

![buscar (cuadro de diálogo)](images/finddialogboxxp.png)

Puede crear y mostrar un cuadro de diálogo **reemplazar** inicializando una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y pasando la estructura a la función [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) . En la ilustración siguiente se muestra un cuadro de diálogo de **reemplazo** típico.

![reemplazar (cuadro de diálogo)](images/replacedialogboxxp.png)

A diferencia de otros cuadros de diálogo comunes, los cuadros de diálogo **Buscar** y **reemplazar** son no modales. Un cuadro de diálogo no modal permite al usuario alternar entre el cuadro de diálogo y la ventana que lo creó. Esto resulta útil para permitir que el usuario busque una cadena, cambie a la ventana de la aplicación para que funcione en la cadena y vuelva al cuadro de diálogo para buscar otra cadena sin repetir el comando necesario para abrir el cuadro de diálogo.

Si la función [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) o [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) crea el cuadro de diálogo correctamente, devuelve un identificador al cuadro de diálogo. Puede usar este identificador para moverse y comunicarse con el cuadro de diálogo. Si la función no puede crear el cuadro de diálogo, devuelve **null**. Puede determinar la causa de un error si llama a la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se tratan los temas siguientes.

-   [El mensaje registrado en FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalización del cuadro de diálogo Buscar o reemplazar](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>El mensaje registrado en FINDMSGSTRING

Antes de crear un cuadro de diálogo **Buscar** o **reemplazar** , debe llamar a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje para el mensaje registrado [**FINDMSGSTRING**](findmsgstring.md) . Después, puede utilizar el identificador para detectar y procesar los mensajes enviados desde el cuadro de diálogo. Cuando el usuario hace clic en el botón **Buscar siguiente**, **reemplazar** o **reemplazar todo** en un cuadro de diálogo, el procedimiento del cuadro de diálogo envía un mensaje **FINDMSGSTRING** al procedimiento de ventana de la ventana propietaria. Al crear el cuadro de diálogo, el miembro **hwndOwner** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica la ventana propietaria.

El parámetro *lParam* de un mensaje [**FINDMSGSTRING**](findmsgstring.md) es un puntero a la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que especificó al crear el cuadro de diálogo. Antes de enviar el mensaje, el cuadro de diálogo establece los miembros de esta estructura con la entrada más reciente del usuario, incluida la cadena que se va a buscar, la cadena de reemplazo (si existe) y las opciones de la operación de búsqueda y reemplazo.

En un mensaje [**FINDMSGSTRING**](findmsgstring.md) , el miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) incluye una de las marcas siguientes para indicar el evento que provocó el mensaje.



| Marca               | Significado                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | El cuadro de diálogo se está cerrando. Una vez que la ventana propietaria procesa este mensaje, el identificador del cuadro de diálogo ya no es válido.                                                                                    |
| **\_BUSCARSIGUIENTE fr**   | El usuario hizo clic en el botón **Buscar siguiente** en un cuadro de diálogo **Buscar** o **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a buscar.                                                         |
| **reemplazar en FR \_**    | El usuario hizo clic en el botón **reemplazar** en un cuadro de diálogo **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo.     |
| **reemplazo de FR \_** | El usuario hizo clic en el botón **reemplazar todo** en un cuadro de diálogo **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo. |



 

En el caso de los mensajes **Buscar siguiente** o **reemplazar todo** , el miembro de **marcas** puede incluir cualquier combinación de las marcas siguientes para indicar las opciones de búsqueda.



| Marca              | Significado                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Francés \_**      | Si se establece, se selecciona el botón **abajo** de los botones de radio dirección, lo que indica que el usuario desea buscar desde la ubicación actual hasta el final del documento. Si no se establece el valor de **fr \_ Down** , se selecciona el botón **subir** para que el usuario desee buscar en el principio del documento.       |
| **\_MATCHCASE MATCHCASE** | Si se establece, se activa la casilla **Coincidir mayúsculas y minúsculas** , lo que indica que el usuario desea que la búsqueda distinga entre mayúsculas y minúsculas. Si no se establece **fr \_ MATCHCASE** , se anula la selección de la casilla para que la búsqueda no distinga mayúsculas de minúsculas.                                                                       |
| **FR \_ WHOLEWORD** | Si se establece, la casilla **coincidir solo con palabras completas** está activada, lo que indica que el usuario desea buscar únicamente palabras completas que coincidan con la cadena de búsqueda. Si no se establece **fr \_ WHOLEWORD** , la casilla está desactivada, por lo que también debe buscar fragmentos de palabras que coincidan con la cadena de búsqueda. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalización del cuadro de diálogo Buscar o reemplazar

Para personalizar un cuadro de diálogo **Buscar** o **reemplazar** , puede usar cualquiera de los métodos siguientes:

-   Especificar valores en la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) al crear el cuadro de diálogo
-   Proporcionar una plantilla personalizada
-   Proporcionar un procedimiento de enlace

Al crear un cuadro de diálogo **Buscar** o **reemplazar** , puede establecer marcas en el miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para ocultar o deshabilitar cualquiera de los controles de opción de búsqueda. Por ejemplo, puede establecer la marca FR \_ NOMATCHCASE para deshabilitar la casilla **Coincidir mayúsculas y minúsculas** o establecer la \_ marca HIDEMATCHCASE fr para ocultarla.

Puede proporcionar una plantilla personalizada para un cuadro de diálogo **Buscar** o **reemplazar** ; por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. Las funciones [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) y [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usan la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para un cuadro de diálogo Buscar o reemplazar**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Textobuscado. Dlg. Los identificadores de control que se usan en la plantilla de cuadro de diálogo **Buscar** o **reemplazar** predeterminada se definen en el archivo Dlgs. h.
2.  Use la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para habilitar la plantilla de la manera siguiente:
    -   -   Si la plantilla personalizada es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca la \_ marca fr ENABLETEMPLATE en el miembro **Flags** . Use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el nombre del módulo y del recurso.

            -O bien-

        -   Si la plantilla personalizada ya está en la memoria, establezca la \_ marca fr ENABLETEMPLATEHANDLE. Use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento de enlace [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) para un cuadro de diálogo **Buscar** o **reemplazar** . El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada para los controles.

**Para habilitar un procedimiento de enlace para un cuadro de diálogo Buscar o reemplazar**

1.  Establezca la \_ marca fr ENABLEHOOK en el miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnHook** .

Después de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento de cuadro de diálogo envía un mensaje de **WM \_ INITDIALOG** al procedimiento de enlace. El parámetro *lParam* de este mensaje es un puntero a la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) usada para inicializar el cuadro de diálogo.

Si el procedimiento de enlace devuelve **false** en respuesta al mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el cuadro de diálogo no se mostrará a menos que el procedimiento de enlace lo muestre. Para ello, primero realice cualquier otra operación Paint y, a continuación, llame a las funciones [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) y [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) . El siguiente fragmento de código muestra un ejemplo:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 