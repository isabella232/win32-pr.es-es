---
description: Los controladores de menús contextuales también se conocen como controladores de menú contextual o controladores de verbos. Un controlador de menú contextual es un tipo de controlador de tipo de archivo.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizar un menú contextual mediante verbos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b33361be5a89480e05bb42bd760b63517bf0b06c9828cae36a36ecddce1e9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968314"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personalizar un menú contextual mediante verbos dinámicos

Los controladores de menús contextuales también se conocen como controladores de menú contextual o controladores de verbos. Un controlador de menú contextual es un tipo de controlador de tipo de archivo.

Este tema se organiza de la siguiente manera:

-   [Acerca de los verbos estáticos y dinámicos](#about-static-and-dynamic-verbs)
-   [Cómo funcionan los controladores de menús contextuales con verbos dinámicos](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Evitar colisiones debido a nombres de verbos no calificados](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrar un controlador de menús contextuales con un verbo dinámico](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementación de la interfaz IContextMenu](#implementing-the-icontextmenu-interface)
    -   [IContextMenu::GetCommandString (Método)](#icontextmenugetcommandstring-method)
    -   [IContextMenu::InvokeCommand (Método)](#icontextmenuinvokecommand-method)
    -   [IContextMenu::QueryContextMenu (Método)](#icontextmenuquerycontextmenu-method)
-   [Temas relacionados](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Acerca de los verbos estáticos y dinámicos

Le recomendamos encarecidamente que implemente un menú contextual mediante uno de los métodos de verbo estático. Se recomienda seguir las instrucciones proporcionadas en la sección "Personalización de un menú contextual mediante verbos estáticos" de Crear controladores [de menú contextual.](context-menu-handlers.md) Para obtener el comportamiento dinámico de verbos estáticos en Windows 7 y versiones posteriores, vea "Getting Dynamic Behavior for Static Verbs" (Obtener comportamiento dinámico para verbos estáticos) en [Creating Context Menu Handlers](context-menu-handlers.md). Para obtener más información sobre la implementación de verbos estáticos y los verbos dinámicos que se deben evitar, vea Elegir un verbo estático o dinámico [para el menú contextual.](shortcut-choose-method.md)

Si debe extender el menú contextual de un tipo de archivo mediante el registro de un verbo dinámico para el tipo de archivo, siga las instrucciones proporcionadas más adelante en este tema.

> [!Note]  
> Hay consideraciones especiales para los Windows de 64 bits al registrar controladores que funcionan en el contexto de aplicaciones de 32 bits: cuando se invocan verbos de Shell en el contexto de una aplicación de 32 bits, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso. Si el controlador .exe está almacenado en una de esas rutas de acceso, no es accesible en este contexto. Por lo tanto, para evitarlo, almacene el .exe en una ruta de acceso que no se redirija o almacene una versión de código auxiliar de la .exe que inicie la versión real.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Cómo funcionan los controladores de menús contextuales con verbos dinámicos

Además de [**IUnknown, los**](/windows/win32/api/unknwn/nn-unknwn-iunknown)controladores de menús contextuales exportan las siguientes interfaces adicionales para controlar la mensajería necesaria para implementar elementos de menú dibujados por el propietario:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorio)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorio)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (opcional)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (opcional)

Para obtener más información sobre los elementos de menú dibujados por el propietario, vea la *sección Creating Owner-Drawn Menu Items* en Using [Menus](../menurc/using-menus.md).

Shell usa la [**interfaz IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar el controlador. Cuando el Shell llama a [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), pasa un objeto de datos con el nombre del objeto y un puntero a una lista de identificadores de elemento (PIDL) de la carpeta que contiene el archivo. El *parámetro hkeyProgID es* la ubicación del Registro en la que se registra el identificador del menú contextual. El **método IShellExtInit::Initialize** debe extraer el nombre de archivo del objeto de datos y almacenar el nombre y el puntero de la carpeta en una lista de identificadores de elemento (PIDL) para su uso posterior. Para obtener más información sobre la inicialización del controlador, [vea Implementing IShellExtInit](handlers.md).

Cuando los verbos se presentan en un menú contextual, primero se detectan, se presentan al usuario y, por último, se invocan. En la lista siguiente se describen estos tres pasos con más detalle:

1.  El shell llama a [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que devuelve un conjunto de verbos que se pueden basar en el estado de los elementos o del sistema.
2.  El sistema pasa un identificador **HMENU** que el método puede usar para agregar elementos al menú contextual.
3.  Si el usuario hace clic en uno de los elementos del controlador, el Shell llama a [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). A continuación, el controlador puede ejecutar el comando adecuado.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Evitar colisiones debido a nombres de verbos no calificados

Dado que los verbos se registran por tipo, se puede usar el mismo nombre de verbo para verbos en distintos elementos. Esto permite a las aplicaciones hacer referencia a verbos comunes independientemente del tipo de elemento. Aunque esta funcionalidad es útil, el uso de nombres no completos puede provocar colisiones con varios proveedores de software independientes (ISV) que eligen el mismo nombre de verbo. Para evitarlo, antefijo siempre los verbos con el nombre del ISV de la manera siguiente:

`ISV_Name.verb`

Use siempre un ProgID específico de la aplicación. La adopción de la convención de asignación de la extensión de nombre de archivo a un PROGID proporcionado por el ISV evita posibles colisiones. Sin embargo, dado que algunos tipos de elementos no usan esta asignación, es necesario usar nombres únicos de proveedor. Al agregar un verbo a un ProgID existente que ya podría tener ese verbo registrado, primero debe quitar la clave del Registro para el verbo anterior antes de agregar su propio verbo. Debe hacerlo para evitar combinar la información del verbo de los dos verbos. Si no lo hace, se produce un comportamiento imprevisible.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrar un controlador de menús contextuales con un verbo dinámico

Los controladores de menú contextual están asociados a un tipo de archivo o a una carpeta. Para los tipos de archivo, el controlador se registra en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Para asociar un controlador de menú contextual a un tipo de archivo o a una carpeta, cree primero una subclave en la subclave **ContextMenuHandlers.** Asigne un nombre a la subclave para el controlador y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador.

A continuación, para asociar un controlador de menú contextual con diferentes tipos de carpetas, registre el controlador de la misma manera que lo haría para un tipo de archivo, pero en la subclave *FolderType* como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Para obtener más información sobre los tipos de carpeta para los que puede registrar controladores, vea [Registrar controladores de extensión de shell](handlers.md).

Si un tipo de archivo tiene un menú contextual asociado, al hacer doble clic en un objeto normalmente se inicia el comando predeterminado y no se llama al método [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del controlador. Para especificar que se debe llamar al método **IContextMenu::QueryContextMenu** del controlador cuando se hace doble clic en un objeto, cree una subclave en la subclave **CLSID** del controlador como se muestra aquí.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Cuando se hace doble clic en un objeto asociado al controlador, se llama a [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) con la marca **\_ CMF DEFAULTONLY** establecida en el *parámetro uFlags.*

Los controladores de menús contextuales deben establecer la subclave **MayChangeDefaultMenu** solo si es posible que necesiten cambiar el verbo predeterminado del menú contextual. Establecer esta subclave obliga al sistema a cargar el archivo DLL del controlador cuando se hace doble clic en un elemento asociado. Si el controlador no cambia el verbo predeterminado, no debe establecer esta subclave porque, al hacerlo, el sistema carga innecesariamente el archivo DLL.

En el ejemplo siguiente se muestran las entradas del Registro que habilitan un controlador de menú contextual para un tipo de archivo .myp. La subclave **CLSID** del controlador incluye una subclave **MayChangeDefaultMenu** para garantizar que se llama al controlador cuando el usuario hace doble clic en un objeto relacionado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>Implementación de la interfaz IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar. Se recomienda encarecidamente implementar un verbo mediante uno de los métodos de verbo estático. Para obtener más información, vea [Elegir un verbo estático o dinámico para el menú contextual.](shortcut-choose-method.md) [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, **GetCommandString,** **InvokeCommand** y **QueryContextMenu,** que se detalló aquí.

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu::GetCommandString (Método)

El método [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo. Este método es opcional. En Windows XP y versiones anteriores de Windows, cuando Windows Explorer tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra Estado de un elemento de menú.

El *parámetro idCmd* contiene el desplazamiento del identificador del comando que se definió cuando se llamó a [**IContextMenu::QueryContextMenu.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GCS \_ HELPTEXTW**. Copie la cadena de ayuda en el *búfer pszName* y conéctela a **un PWSTR**. La cadena de verbo se solicita estableciendo *uFlags* en **GCS \_ VERBW**. Copie la cadena adecuada en *pszName,* igual que con la cadena de ayuda. Los controladores de menús contextuales no usan las marcas **\_ VALIDATEA** y **\_ GCS VALIDATEW de GCS.**

En el ejemplo siguiente se muestra una implementación sencilla de [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección Método [IContextMenu::QueryContextMenu](#icontextmenuquerycontextmenu-method) de este tema. Dado que el controlador agrega solo un elemento de menú, solo se puede devolver un conjunto de cadenas. El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.

La [**función StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName* para asegurarse de que la cadena copiada no supera el tamaño del búfer especificado por *cchName*. En este ejemplo solo se implementa la compatibilidad con los valores Unicode de *uFlags*, porque solo se han usado en Windows Explorer desde Windows 2000.


```C++
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
                // to discover the canonical name for the verb passed in
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

Se llama a este método cuando un usuario hace clic en un elemento de menú para decir al controlador que ejecute el comando asociado. El *parámetro pici* apunta a una estructura que contiene la información necesaria.

Aunque *pici* se declara en Shlobj.h como una estructura [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que hacen posible pasar cadenas Unicode.

Compruebe el **miembro cbSize** de *pici* para determinar qué estructura se pasó. Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la marca **\_ \_ UNICODE CMIC MASK,** convierte *pici* en **CMINVOKECOMMANDINFOEX**. Esto permite que la aplicación use la información Unicode contenida en los últimos cinco miembros de la estructura .

El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar. Los comandos se identifican de una de las dos maneras siguientes:

-   Por la cadena verbal del comando
-   Por el desplazamiento del identificador del comando

Para distinguir entre estos dos casos, compruebe la palabra de orden superior **de lpVerb** para el caso ANSI o **lpVerbW** para el caso Unicode. Si la palabra de orden alto es distinta de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo. Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden bajo **de lpVerb.**

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) proporcionados antes y después de esta sección. El método determina primero qué estructura se pasa. A continuación, determina si el comando se identifica mediante su desplazamiento o su verbo. Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válidos, el método muestra un cuadro de mensaje.


```C++
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

El desplazamiento de comandos de un identificador *de elemento* es la diferencia entre el identificador y el valor de *idCmdFirst.* Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual porque shell podría usarlo para identificar el elemento si posteriormente llama a [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

También debe asignar un [verbo](launch.md) a cada comando que agregue. Un verbo es una cadena que se puede usar en lugar del desplazamiento para identificar el comando cuando se llama a [**IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.

Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menú contextual. Se describen en la tabla siguiente.



| Marca             | Descripción                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto. [**IContextMenu::QueryContextMenu debe**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) devolver el control al shell sin modificar el menú. |
| CMF \_ NODEFAULT   | Ningún elemento del menú debe ser el elemento predeterminado. El método debe agregar sus comandos al menú.                                                                                                                          |
| CMF \_ NORMAL      | El menú contextual se mostrará normalmente. El método debe agregar sus comandos al menú.                                                                                                                            |



 

Use [**InsertMenu o**](/windows/win32/api/winuser/nf-winuser-insertmenua) [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista. A continuación, **devuelva un valor HRESULT** con la gravedad establecida en **SEVERITY \_ SUCCESS**. Establezca el valor de código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1). Por ejemplo, suponga que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8. El valor devuelto debe ser `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando. El desplazamiento del identificador del comando es IDM \_ DISPLAY, que se establece en cero. Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en formatos ANSI y Unicode.


```C++
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



Para otras tareas de implementación de verbos, vea [Crear controladores de menú contextual.](context-menu-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús contextuales y controladores de menús contextuales](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple](verbs-best-practices.md)
</dt> <dt>

[Creación de controladores de menús contextuales](context-menu-handlers.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 
