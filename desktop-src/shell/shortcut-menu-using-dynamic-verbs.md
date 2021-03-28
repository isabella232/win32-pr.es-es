---
description: Los controladores de menús contextuales también se denominan controladores de menú contextual o controladores de verbos. Un controlador de menú contextual es un tipo de controlador de tipo de archivo.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalización de un menú contextual mediante verbos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985751"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personalización de un menú contextual mediante verbos dinámicos

Los controladores de menús contextuales también se denominan controladores de menú contextual o controladores de verbos. Un controlador de menú contextual es un tipo de controlador de tipo de archivo.

Este tema se organiza de la siguiente manera:

-   [Acerca de los verbos estáticos y dinámicos](#about-static-and-dynamic-verbs)
-   [Cómo funcionan los controladores de menú contextual con verbos dinámicos](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Evitar colisiones debido a nombres de verbo no completos](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrar un controlador de menú contextual con un verbo dinámico](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementar la interfaz IContextMenu](#implementing-the-icontextmenu-interface)
    -   [IContextMenu:: GetCommandString (método)](#icontextmenugetcommandstring-method)
    -   [IContextMenu:: InvokeCommand (método)](#icontextmenuinvokecommand-method)
    -   [IContextMenu:: QueryContextMenu (método)](#icontextmenuquerycontextmenu-method)
-   [Temas relacionados](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Acerca de los verbos estáticos y dinámicos

Le recomendamos encarecidamente que implemente un menú contextual con uno de los métodos estáticos Verb. Se recomienda seguir las instrucciones proporcionadas en la sección "personalizar un menú contextual mediante verbos estáticos" de [creación de controladores de menú contextuales](context-menu-handlers.md). Para obtener el comportamiento dinámico de los verbos estáticos en Windows 7 y versiones posteriores, vea el tema sobre cómo obtener el comportamiento dinámico para verbos estáticos en [creación de controladores de menú contextuales](context-menu-handlers.md). Para obtener información detallada sobre la implementación de verbos estáticos y los verbos dinámicos que se deben evitar, vea [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md).

Si debe extender el menú contextual de un tipo de archivo registrando un verbo dinámico para el tipo de archivo, siga las instrucciones que se proporcionan más adelante en este tema.

> [!Note]  
> Existen consideraciones especiales para Windows de 64 bits al registrar controladores que funcionan en el contexto de las aplicaciones de 32 bits: cuando los verbos de Shell se invocan en el contexto de una aplicación de 32 bits, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso. Si el controlador. exe se almacena en una de esas rutas de acceso, no es accesible en este contexto. Por lo tanto, como solución alternativa, almacene el archivo. exe en una ruta de acceso que no se redirija, o bien almacene una versión de código auxiliar del archivo. exe que inicia la versión real.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Cómo funcionan los controladores de menú contextual con verbos dinámicos

Además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), los controladores de menú contextual exportan las siguientes interfaces adicionales para controlar la mensajería necesaria para implementar elementos de menú dibujados por el propietario:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorio)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorio)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (opcional)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (opcional)

Para obtener más información sobre los elementos de menú dibujados por el propietario, consulte la sección *creación de Owner-Drawn elementos de menú* en [uso de menús](../menurc/using-menus.md).

Shell usa la interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar el controlador. Cuando el shell llama a [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), pasa un objeto de datos con el nombre del objeto y un puntero a una lista de identificadores de elemento (PIDL) de la carpeta que contiene el archivo. El parámetro *hkeyProgID* es la ubicación del registro en la que se registra el identificador del menú contextual. El método **IShellExtInit:: Initialize** debe extraer el nombre de archivo del objeto de datos y almacenar el nombre y el puntero de la carpeta en una lista de identificadores de elemento (PIDL) para su uso posterior. Para obtener más información sobre la inicialización del controlador, vea [implementar IShellExtInit](handlers.md).

Cuando los verbos se presentan en un menú contextual, se detectan primero y, a continuación, se presentan al usuario y, por último, se invocan. En la lista siguiente se describen estos tres pasos con más detalle:

1.  El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que devuelve un conjunto de verbos que pueden basarse en el estado de los elementos o del sistema.
2.  El sistema pasa un identificador **HMENU** que el método puede usar para agregar elementos al menú contextual.
3.  Si el usuario hace clic en uno de los elementos del controlador, el shell llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). Después, el controlador puede ejecutar el comando adecuado.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Evitar colisiones debido a nombres de verbo no completos

Dado que los verbos se registran por tipo, se puede usar el mismo nombre de verbo para los verbos en elementos diferentes. Esto permite que las aplicaciones hagan referencia a verbos comunes independientes del tipo de elemento. Aunque esta funcionalidad es útil, el uso de nombres no completos puede producir colisiones con varios fabricantes de software independientes (ISV) que elijan el mismo nombre de verbo. Para evitar esto, debe prefijar siempre los verbos con el nombre de ISV como se indica a continuación:

`ISV_Name.verb`

Use siempre un ProgID específico de la aplicación. La adopción de la Convención de asignación de la extensión de nombre de archivo a un ProgID proporcionado por ISV evita posibles colisiones. Sin embargo, dado que algunos tipos de elemento no usan esta asignación, es necesario usar nombres únicos de proveedor. Al agregar un verbo a un ProgID existente que ya tiene el verbo registrado, primero debe quitar la clave del registro del verbo anterior antes de agregar su propio verbo. Debe hacerlo para evitar la combinación de la información del verbo de los dos verbos. Si no lo hace, se producirá un comportamiento imprevisible.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrar un controlador de menú contextual con un verbo dinámico

Los controladores de menú contextual están asociados a un tipo de archivo o a una carpeta. En el caso de los tipos de archivo, el controlador se registra en la subclave siguiente.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Para asociar un controlador de menú contextual con un tipo de archivo o una carpeta, primero cree una subclave en la subclave **ContextMenuHandlers** . Asigne un nombre a la subclave del controlador y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador.

Después, para asociar un controlador de menú contextual con distintos tipos de carpetas, registre el controlador del mismo modo que lo haría para un tipo de archivo, pero en la subclave *FolderType* , tal y como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Para obtener más información acerca de los tipos de carpetas para los que puede registrar controladores, consulte [registrar controladores de extensión de Shell](handlers.md).

Si un tipo de archivo tiene un menú contextual asociado, al hacer doble clic en un objeto se inicia normalmente el comando predeterminado y no se llama al método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del controlador. Para especificar que se debe llamar al método **IContextMenu:: QueryContextMenu** del controlador cuando se hace doble clic en un objeto, cree una subclave en la subclave **CLSID** del controlador, como se muestra aquí.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Cuando se hace doble clic en un objeto asociado al controlador, se llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) con la marca **CMF \_ DEFAULTONLY** establecida en el parámetro *uFlags* .

Los controladores de menú contextual solo deben establecer la subclave **MayChangeDefaultMenu** si es posible que necesiten cambiar el verbo predeterminado del menú contextual. Al establecer esta subclave, el sistema carga el archivo DLL del controlador cuando se hace doble clic en un elemento asociado. Si el controlador no cambia el verbo predeterminado, no debe establecer esta subclave, ya que esto hace que el sistema cargue el archivo DLL innecesariamente.

En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de menú contextual para un tipo de archivo. MYP. La subclave **CLSID** del controlador incluye una subclave **MayChangeDefaultMenu** para garantizar que se llama al controlador cuando el usuario hace doble clic en un objeto relacionado.

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

## <a name="implementing-the-icontextmenu-interface"></a>Implementar la interfaz IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar. Se recomienda encarecidamente implementar un verbo utilizando uno de los métodos estáticos Verb. Para obtener más información, vea [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, **GetCommandString**, **InvokeCommand** y **QueryContextMenu**, que se describen aquí en detalle.

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu:: GetCommandString (método)

El método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo. Este método es opcional. En Windows XP y versiones anteriores de Windows, cuando el explorador de Windows tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra de estado de un elemento de menú.

El parámetro *idCmd* contiene el desplazamiento de identificador del comando que se definió cuando se llamó a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GC \_ HELPTEXTW**. Copie la cadena de ayuda en el búfer de *pszName empiezan* , convirtiéndola en un **PWSTR**. La cadena de verbo se solicita estableciendo *uFlags* en **GC \_ VERBW**. Copie la cadena adecuada en *pszName empiezan*, al igual que con la cadena de ayuda. Los controladores de menú contextual no usan las marcas **GC \_ validatea** y **GC \_ VALIDATEW** .

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección del [método IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) de este tema. Dado que el controlador solo agrega un elemento de menú, solo hay un conjunto de cadenas que se pueden devolver. El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.

La función [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName empiezan* para asegurarse de que la cadena copiada no supera el tamaño del búfer especificado por *cchName*. En este ejemplo solo se implementa la compatibilidad con los valores Unicode de *uFlags*, ya que solo se han utilizado en el explorador de Windows desde Windows 2000.


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



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu:: InvokeCommand (método)

Se llama a este método cuando un usuario hace clic en un elemento de menú para indicar al controlador que ejecute el comando asociado. El parámetro *pici* apunta a una estructura que contiene la información requerida.

Aunque *pici* se declara en ShlObj. h como una estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que permiten pasar cadenas Unicode.

Compruebe el miembro **cbSize** de *pici* para determinar la estructura que se ha pasado. Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la **marca \_ \_ Unicode CMIC Mask** , convierta *pici* en **CMINVOKECOMMANDINFOEX**. Esto permite que la aplicación use la información Unicode contenida en los cinco últimos miembros de la estructura.

El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar. Los comandos se identifican de una de las dos maneras siguientes:

-   Por la cadena de verbo del comando
-   Por el desplazamiento del identificador del comando

Para distinguir entre estos dos casos, Compruebe la palabra de orden superior de **lpVerb** para el caso ANSI o **lpVerbW** para el caso de Unicode. Si la palabra de orden superior es distinto de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo. Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden inferior de **lpVerb**.

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) y [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) especificados antes y después de esta sección. El método determina primero la estructura que se va a pasar. A continuación, determina si el comando se identifica por su desplazamiento o por su verbo. Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válido, el método muestra un cuadro de mensaje.


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



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu:: QueryContextMenu (método)

El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar el controlador de menú contextual para agregar sus elementos de menú al menú. Pasa el identificador **HMENU** en el parámetro *HMENU* . El parámetro *indexMenu* se establece en el índice que se va a usar para el primer elemento de menú que se va a agregar.

Los elementos de menú que agregue el controlador deben tener identificadores que se encuentren entre los valores de los parámetros *idCmdFirst* y *idCmdLast* . Normalmente, el primer identificador de comando se establece en *idCmdFirst*, que se incrementa en uno (1) para cada comando adicional. Esta práctica le ayuda a evitar superar *idCmdLast* y maximiza el número de identificadores disponibles en caso de que el shell llame a más de un controlador.

El *desplazamiento de comandos* de un identificador de elemento es la diferencia entre el identificador y el valor de *idCmdFirst*. Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual porque el shell podría utilizarlo para identificar el elemento si después llama a [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

También debe asignar un [verbo](launch.md) a cada comando que agregue. Un verbo es una cadena que se puede utilizar en lugar del desplazamiento para identificar el comando cuando se llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.

Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menús contextuales. Se describen en la tabla siguiente.



| Marca             | Descripción                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto. [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) debe devolver el control al shell sin modificar el menú. |
| CMF \_ NOdefault   | Ningún elemento del menú debe ser el elemento predeterminado. El método debe agregar sus comandos al menú.                                                                                                                          |
| CMF \_ normal      | El menú contextual se mostrará normalmente. El método debe agregar sus comandos al menú.                                                                                                                            |



 

Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista. A continuación, devuelva un valor **HRESULT** con la gravedad establecida en **Severity \_ Success**. Establezca el valor del código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1). Por ejemplo, supongamos que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8. El valor devuelto debe ser `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando. El desplazamiento de identificador del comando es la visualización de IDM \_ , que se establece en cero. Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en los formatos ANSI y Unicode.


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



Para otras tareas de implementación de verbos, vea [crear controladores de menús contextuales](context-menu-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús contextuales y controladores de menú contextual](context-menu.md)
</dt> <dt>

[Verbos y asociaciones de archivo](fa-verbs.md)
</dt> <dt>

[Elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md)
</dt> <dt>

[Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección](verbs-best-practices.md)
</dt> <dt>

[Crear controladores de menú contextual](context-menu-handlers.md)
</dt> <dt>

[Referencia del menú contextual](context-menu-reference.md)
</dt> </dl>

 

 
