---
description: IContextMenu es la interfaz más eficaz, pero también la más complicada de implementar.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Cómo implementar la interfaz IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001905"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Cómo implementar la interfaz IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es la interfaz más eficaz, pero también la más complicada de implementar. Se recomienda encarecidamente implementar un verbo utilizando uno de los métodos estáticos Verb. Para obtener más información, vea [elegir un método de menú contextual estático o dinámico](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)y [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que se describen aquí en detalle.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   C++

### <a name="prerequisites"></a>Requisitos previos

-   Verbo estático
-   Menú contextual

## <a name="instructions"></a>Instrucciones

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu:: GetCommandString (método)

El método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo. Este método es opcional. En Windows XP y versiones anteriores de Windows, cuando el explorador de Windows tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra de estado de un elemento de menú.

El parámetro *idCmd* contiene el desplazamiento de identificador del comando que se definió cuando se llamó a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GC \_ HELPTEXTW**. Copie la cadena de ayuda en el búfer de *pszName empiezan* , convirtiéndola en un **PWSTR**. La cadena de verbo se solicita estableciendo *uFlags* en **GC \_ VERBW**. Copie la cadena adecuada en *pszName empiezan*, al igual que con la cadena de ayuda. Los controladores de menú contextual no usan las marcas **GC \_ validatea** y **GC \_ VALIDATEW** .

En el ejemplo siguiente se muestra una implementación simple de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección [IContextMenu:: QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) de este tema. Dado que el controlador solo agrega un elemento de menú, solo hay un conjunto de cadenas que se pueden devolver. El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.

La función [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName empiezan* para asegurarse de que la cadena copiada no supera el tamaño del búfer especificado por *cchName*. En este ejemplo solo se implementa la compatibilidad con los valores Unicode de *uFlags*, ya que solo se han utilizado en el explorador de Windows desde Windows 2000.


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



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu:: InvokeCommand (método)

Se llama a este método cuando un usuario hace clic en un elemento de menú para indicar al controlador que ejecute el comando asociado. El parámetro *pici* apunta a una estructura que contiene la información necesaria para ejecutar el comando.

Aunque *pici* se declara en ShlObj. h como una estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que permiten pasar cadenas Unicode.

Compruebe el miembro **cbSize** de *pici* para determinar la estructura que se ha pasado. Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la **marca \_ \_ Unicode CMIC Mask** , convierta *pici* en **CMINVOKECOMMANDINFOEX**. Esto permite que la aplicación use la información Unicode contenida en los cinco últimos miembros de la estructura.

El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar. Los comandos se identifican de una de las dos maneras siguientes:

-   Por la cadena de verbo del comando
-   Por el desplazamiento del identificador del comando

Para distinguir entre estos dos casos, Compruebe la palabra de orden superior de **lpVerb** para el caso ANSI o **lpVerbW** para el caso de Unicode. Si la palabra de orden superior es distinto de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo. Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden inferior de **lpVerb**.

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) y [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) especificados antes y después de esta sección. El método determina primero la estructura que se va a pasar. A continuación, determina si el comando se identifica por su desplazamiento o por su verbo. Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válido, el método muestra un cuadro de mensaje.


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



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu:: QueryContextMenu (método)

El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar el controlador de menú contextual para agregar sus elementos de menú al menú. Pasa el identificador **HMENU** en el parámetro *HMENU* . El parámetro *indexMenu* se establece en el índice que se va a usar para el primer elemento de menú que se va a agregar.

Los elementos de menú que agregue el controlador deben tener identificadores que se encuentren entre los valores de los parámetros *idCmdFirst* y *idCmdLast* . Normalmente, el primer identificador de comando se establece en *idCmdFirst*, que se incrementa en uno (1) para cada comando adicional. Esta práctica le ayuda a evitar superar *idCmdLast* y maximiza el número de identificadores disponibles en caso de que el shell llame a más de un controlador.

El *desplazamiento de comandos* de un identificador de elemento es la diferencia entre el identificador y el valor de *idCmdFirst*. Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual, porque el shell podría usar el desplazamiento para identificar el elemento si después llama a [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

También debe asignar un [verbo](launch.md) a cada comando que agregue. Un verbo es una cadena que se puede utilizar en lugar del desplazamiento para identificar el comando cuando se llama a [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.

Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menús contextuales. Se describen en la tabla siguiente.



| Marca             | Descripción                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto. [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) debe devolver el control al shell sin modificar el menú. |
| CMF \_ NOdefault   | Ningún elemento del menú debe ser el elemento predeterminado. El método debe agregar sus comandos al menú.                                                                                                                          |
| CMF \_ normal      | El menú contextual se mostrará normalmente. El método debe agregar sus comandos al menú.                                                                                                                            |



 

Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista. A continuación, devuelva un valor **HRESULT** con la gravedad establecida en Severity \_ Success. Establezca el valor del código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1). Por ejemplo, supongamos que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8. El valor devuelto debe ser MAKE \_ HRESULT (Severity \_ Success, 0, 8 + 1).

En el ejemplo siguiente se muestra una implementación simple de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando. El desplazamiento de identificador del comando es la visualización de IDM \_ , que se establece en cero. Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en los formatos ANSI y Unicode.


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



## <a name="remarks"></a>Observaciones

Para otras tareas de implementación de verbos, vea [crear controladores de menús contextuales](context-menu-handlers.md).

 

 
