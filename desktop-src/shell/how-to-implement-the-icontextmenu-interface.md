---
description: IContextMenu es la interfaz más eficaz, pero también la más complicada de implementar.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Cómo implementar la interfaz IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223472"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Cómo implementar la interfaz IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es la interfaz más eficaz, pero también la más complicada de implementar. Se recomienda encarecidamente implementar un verbo mediante uno de los métodos de verbo estáticos. Para obtener más información, vea [Elegir un método de menú contextual estático o dinámico](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, [**GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)y [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)que se detalló aquí.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   C++

### <a name="prerequisites"></a>Requisitos previos

-   Verbo estático
-   Menú contextual

## <a name="instructions"></a>Instrucciones

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu::GetCommandString (Método)

El método [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo. Este método es opcional. En Windows XP y versiones anteriores de Windows, cuando Windows Explorer tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra de estado de un elemento de menú.

El *parámetro idCmd* contiene el desplazamiento del identificador del comando que se definió cuando se llamó a [**IContextMenu::QueryContextMenu.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GCS \_ HELPTEXTW**. Copie la cadena de ayuda en el *búfer pszName* y conéctela en **un PWSTR**. La cadena de verbo se solicita estableciendo *uFlags* en **GCS \_ VERBW**. Copie la cadena adecuada en *pszName,* igual que con la cadena de ayuda. Los controladores de menú contextual no usan las marcas **\_ VALIDATEA** y **\_ GCS VALIDATEW de GCS.**

En el ejemplo siguiente se muestra una implementación simple de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección [Método IContextMenu::QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) de este tema. Dado que el controlador agrega solo un elemento de menú, solo se puede devolver un conjunto de cadenas. El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.

La [**función StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName* para asegurarse de que la cadena copiada no supere el tamaño del búfer especificado por *cchName*. En este ejemplo solo se implementa compatibilidad con los valores Unicode de *uFlags*, ya que solo se han usado en Windows Explorer desde Windows 2000.


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu::InvokeCommand (Método)

Se llama a este método cuando un usuario hace clic en un elemento de menú para decir al controlador que ejecute el comando asociado. El *parámetro pici* apunta a una estructura que contiene la información necesaria para ejecutar el comando.

Aunque *pici* se declara en Shlobj.h como una estructura [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que hacen posible pasar cadenas Unicode.

Compruebe el **miembro cbSize** de *pici* para determinar qué estructura se ha pasado. Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la marca UNICODE MASK de **CMIC, \_ \_** convierte *pici* en **CMINVOKECOMMANDINFOEX**. Esto permite que la aplicación use la información Unicode contenida en los últimos cinco miembros de la estructura.

El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar. Los comandos se identifican de una de las dos maneras siguientes:

-   Por la cadena de verbo del comando
-   Por el desplazamiento del identificador del comando

Para distinguir entre estos dos casos, compruebe la palabra de orden superior **lpVerb** para el caso ANSI o **lpVerbW** para el caso Unicode. Si la palabra de orden alto es distinta de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo. Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden bajo **de lpVerb.**

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) proporcionados antes y después de esta sección. El método determina primero qué estructura se pasa. A continuación, determina si el comando se identifica mediante su desplazamiento o su verbo. Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válidos, el método muestra un cuadro de mensaje.


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu::QueryContextMenu (Método)

El shell llama [**a IContextMenu::QueryContextMenu para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) permitir que el controlador de menús contextuales agregue sus elementos de menú al menú. Pasa el identificador **HMENU** en el *parámetro hmenu.* El *parámetro indexMenu* se establece en el índice que se va a usar para el primer elemento de menú que se va a agregar.

Los elementos de menú agregados por el controlador deben tener identificadores que se encuentran entre los valores de los parámetros *idCmdFirst* *e idCmdLast.* Normalmente, el primer identificador de comando se establece en *idCmdFirst*, que se incrementa en uno (1) para cada comando adicional. Esta práctica le ayuda a evitar superar *idCmdLast* y maximiza el número de identificadores disponibles en caso de que el Shell llame a más de un controlador.

El desplazamiento del comando de un identificador *de elemento* es la diferencia entre el identificador y el valor de *idCmdFirst*. Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual, ya que shell podría usar el desplazamiento para identificar el elemento si posteriormente llama a [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

También debe asignar un [verbo](launch.md) a cada comando que agregue. Un verbo es una cadena que se puede usar en lugar del desplazamiento para identificar el comando cuando se llama a [**InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.

Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menú contextual. Se describen en la tabla siguiente.



| Marca             | Descripción                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto. [**IContextMenu::QueryContextMenu debe**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) devolver el control al shell sin modificar el menú. |
| CMF \_ NODEFAULT   | Ningún elemento del menú debe ser el elemento predeterminado. El método debe agregar sus comandos al menú.                                                                                                                          |
| CMF \_ NORMAL      | El menú contextual se mostrará normalmente. El método debe agregar sus comandos al menú.                                                                                                                            |



 

Use [**InsertMenu o**](/windows/win32/api/winuser/nf-winuser-insertmenua) [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista. A continuación, **devuelva un valor HRESULT** con la gravedad establecida en SEVERITY \_ SUCCESS. Establezca el valor de código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1). Por ejemplo, suponga que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8. El valor devuelto debe ser MAKE \_ HRESULT(SEVERITY \_ SUCCESS, 0, 8 + 1).

En el ejemplo siguiente se muestra una implementación sencilla [**de QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando. El desplazamiento del identificador del comando es IDM \_ DISPLAY, que se establece en cero. Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en formato ANSI y Unicode.


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Comentarios

Para otras tareas de implementación de verbos, vea [Crear controladores de menús contextuales.](context-menu-handlers.md)

 

 
