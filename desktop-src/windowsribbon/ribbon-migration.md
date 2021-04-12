---
title: Migrar al marco de cinta de Windows
description: Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario enriquecida, dinámica y controlada por contexto del sistema de comandos de la cinta de opciones de Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Cinta de Windows, migrar a
- Cinta de opciones, migrar a
- migrar a la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487959"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>Migrar al marco de cinta de Windows

Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario enriquecida, dinámica y controlada por contexto del sistema de comandos de la cinta de opciones de Windows. Esta es una manera fácil y eficaz de modernizar y revitalizar la aplicación, a la vez que mejora la accesibilidad, la facilidad de uso y la capacidad de detección de su funcionalidad.

## <a name="introduction"></a>Introducción

En general, la migración de una aplicación existente al marco de la cinta de opciones implica lo siguiente:

-   Diseñar un diseño de cinta y controlar la organización que expone la funcionalidad de la aplicación existente y es lo suficientemente flexible como para admitir nuevas funcionalidades.
-   Adaptación del código de la aplicación existente.
-   Migrar los recursos de la aplicación existentes (cadenas e imágenes) al marco de la cinta de opciones.

> [!Note]  
> Las [instrucciones](https://msdn.microsoft.com/library/cc872782.aspx) para la experiencia del usuario de la cinta deben revisarse para determinar si la aplicación es una candidata adecuada para una interfaz de usuario de la cinta de opciones.

 

## <a name="design-the-ribbon-layout"></a>Diseñar el diseño de la cinta de opciones

Se pueden identificar diseños de interfaz de usuario de cinta potenciales y diseños de control siguiendo estos pasos:

1.  Realizar el inventario de toda la funcionalidad existente.
2.  Convertir esta funcionalidad en comandos de la cinta de opciones.
3.  Organizar los comandos en grupos lógicos.

### <a name="take-inventory"></a>Realizar inventario

En el marco de la cinta de opciones, la funcionalidad expuesta por una aplicación que manipula el estado o la vista de un área de trabajo o documento se considera un comando. Lo que constituye un comando puede variar y depende de la naturaleza y el dominio de la aplicación existente.

En la tabla siguiente se muestra un conjunto de comandos básicos para una aplicación de edición de texto hipotética:



| Símbolo           | id     | Descripción               |
|------------------|--------|---------------------------|
| archivo de ID. \_ \_ nuevo    | 0xE100 | Nuevo documento              |
| archivo de identificador \_ \_ guardado   | 0xE103 | Guardar documento             |
| archivo de ID. \_ \_ guardado | 0xE104 | Guardar como... diálogo       |
| IDENTIFICADOR de \_ archivo \_ abierto   | 0xE101 | Abrir... diálogo          |
| \_salida de archivo de identificador \_   | 0xE102 | Salir de la aplicación      |
| deshacer edición de ID. \_ \_   | 0xE12B | Deshacer                      |
| \_cortar edición de ID. \_    | 0xE123 | Cortar el texto seleccionado         |
| \_editar la \_ copia de edición   | 0xE122 | Copiar texto seleccionado        |
| \_pegar edición de ID. \_  | 0xE125 | Pegar texto del portapapeles |
| \_borrado de edición de ID. \_  | 0xE120 | Eliminar texto seleccionado      |
| \_zoom de vista de identificador \_   | 1242   | Acercar... diálogo          |



 

Mire más allá de los menús y las barras de herramientas existentes al crear un inventario de comandos. Tenga en cuenta todas las formas en que un usuario puede interactuar con el área de trabajo. Aunque no todos los comandos son adecuados para su inclusión en la cinta de opciones, este ejercicio puede exponer muy bien comandos ocultos previamente por capas de la interfaz de usuario.

### <a name="translate"></a>Translate

No todos los comandos deben representarse en la interfaz de usuario de la cinta de opciones. Por ejemplo, al escribir texto, cambiar una selección, desplazarse o mover el punto de inserción con el mouse todos los comandos se pueden incluir en el editor de texto hipotético, sin embargo, estos no son adecuados para exponer en una barra de comandos, ya que cada uno implica una interacción directa con la interfaz de usuario de la aplicación.

Por el contrario, algunas funciones no se pueden considerar como un comando en el sentido tradicional. Por ejemplo, en lugar de estar escondido en un cuadro de diálogo, los ajustes de los márgenes de la página de la impresora se pueden representar en la cinta de opciones como un grupo de controles de número en una pestaña o [modo de aplicación](ribbon-applicationmodes.md)contextual.

> [!Note]  
> Anote el identificador numérico que se puede asignar a cada comando. Algunos marcos de interfaz de usuario, como Microsoft Foundation Classes (MFC), definen identificadores para comandos como el menú Archivo y edición (0xE100 a 0xE200).

 

### <a name="organize"></a>Organizar

Antes de intentar organizar el inventario de comandos, se deben revisar las directrices de la [experiencia del usuario](https://msdn.microsoft.com/library/cc872782.aspx) en la cinta para obtener los procedimientos recomendados al implementar una interfaz de usuario de la cinta.

En general, se pueden aplicar las siguientes reglas a la organización de comandos de la cinta de opciones:

-   Es más probable que los comandos que operan en el archivo o en la aplicación global pertenezcan al menú de la [aplicación](windowsribbon-controls-applicationmenu.md).
-   Los comandos usados con frecuencia, como cortar, copiar y pegar (como en el ejemplo del editor de texto), normalmente se colocan en una pestaña Inicio predeterminada. En aplicaciones más complejas, se pueden duplicar en otra parte de la interfaz de usuario de la cinta de opciones.
-   Los comandos importantes o usados con frecuencia podrían garantizar la inclusión predeterminada en la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md).

El marco de la cinta de opciones también proporciona controles ContextMenu y MiniToolbar a través de la vista ContextPopup. Estas características no son obligatorias, pero si la aplicación tiene uno o varios menús contextuales existentes, la migración de los comandos que contienen puede permitir la reutilización del código base existente con el enlace automático a los recursos existentes.

Dado que cada aplicación es diferente, lea las instrucciones e intente aplicarlas a la máxima medida posible. Uno de los objetivos del marco de la cinta de opciones es proporcionar una experiencia de usuario familiar y coherente, y este objetivo será más factible si los diseños de nuevas aplicaciones reflejan las aplicaciones de cinta existentes lo máximo posible.

## <a name="adapt-your-code"></a>Adaptación del código

Una vez que los comandos de la cinta de opciones se han identificado y organizado en agrupaciones lógicas, el número de pasos implicados al incorporar el marco de cinta en el código de aplicación existente depende de la complejidad de la aplicación original. En general, hay tres pasos básicos:

-   Cree el marcado de la cinta de opciones en función de la organización de comandos y la especificación de diseño.
-   Reemplazar la funcionalidad heredada de menús y barras de herramientas por la funcionalidad de la cinta.
-   Implemente un adaptador de IUICommandHandler.

### <a name="create-the-markup"></a>Crear el marcado

La lista de comandos, así como su organización y diseño, se declaran a través del archivo de marcado de la cinta de opciones utilizado por el [compilador de marcado](windowsribbon-intentcl.md)de la cinta.

> [!Note]  
> Muchos de los pasos necesarios para adaptar una aplicación existente son similares a los necesarios para iniciar una nueva aplicación de cinta. Para obtener más información, consulte el tutorial [creación de una aplicación de cinta](windowsribbon-stepbystep.md) para obtener una nueva aplicación de cinta.

 

Hay dos secciones principales en el marcado de la cinta de opciones. La primera sección es un manifiesto de comandos y sus recursos asociados (cadenas e imágenes). La segunda sección especifica la estructura y la ubicación de los controles en la cinta de opciones.

El marcado para el editor de texto simple podría ser similar al del ejemplo siguiente:

> [!Note]  
> Los recursos de imagen y de cadena se describen más adelante en este artículo.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Para evitar la redefinición de símbolos definidos por un marco de interfaz de usuario como MFC, en el ejemplo anterior se usan nombres de símbolos ligeramente diferentes para cada comando (archivo de ID. \_ \_ nuevo frente a ID \_ cmd \_ nuevo). Sin embargo, el identificador numérico asignado a cada comando debe ser el mismo.

Para integrar el archivo de marcado en una aplicación, configure un paso de compilación personalizada para ejecutar el compilador de marcado de la cinta de opciones UICC.exe. El encabezado y los archivos de recursos resultantes se incorporan en el proyecto existente. Si la aplicación de la cinta de opciones editor de texto de ejemplo se denomina "RibbonPad", se requiere una línea de comandos de compilación personalizada similar a la siguiente:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



El compilador de marcado crea un archivo binario, un archivo de encabezado (H) y un archivo de recursos (RC). Dado que es probable que la aplicación existente tenga un archivo RC existente, incluya los archivos H y RC generados en ese archivo RC, tal como se muestra en el ejemplo siguiente:


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Reemplazar barras de herramientas y menús heredados

Reemplazar los menús y las barras de herramientas estándar con una cinta de opciones en una aplicación heredada requiere lo siguiente:

1.  Quite las referencias de recursos de menús y barras de herramientas del archivo de recursos de la aplicación.
2.  Elimine todo el código de inicialización de la barra de herramientas y del menú.
3.  Elimine cualquier código utilizado para adjuntar una barra de herramientas o una barra de menús a la ventana de nivel superior de la aplicación.
4.  Cree una instancia del marco de la cinta de opciones.
5.  Adjunte la cinta de opciones a la ventana de nivel superior de la aplicación.
6.  Cargar el marcado compilado.

> [!IMPORTANT]
> La barra de estado y las tablas de métodos abreviados de teclado existentes deben conservarse, ya que el marco de cinta no reemplaza estas características.

 

En el ejemplo siguiente se muestra cómo inicializar el marco de trabajo mediante [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



En el ejemplo siguiente se muestra cómo usar [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para cargar el marcado compilado:


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



La clase CApplication, a la que se hace referencia anteriormente, debe implementar un par de interfaces del modelo de objetos componentes (COM) definidas por el marco de la cinta de opciones: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) y [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) proporciona la interfaz de devolución de llamada principal entre el marco de trabajo y la aplicación (por ejemplo, el alto de la cinta de opciones se comunica a través de [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) mientras que las devoluciones de llamada para comandos individuales se proporcionan en respuesta a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).

**Sugerencia:** Algunos marcos de trabajo de la aplicación, como MFC, requieren que se tenga en cuenta el alto de la barra de cinta al representar el espacio de documento de la aplicación. En estos casos, es necesario agregar una ventana oculta para superponer la barra de cinta y forzar el espacio del documento al alto deseado. Para obtener un ejemplo de este enfoque, en el que se llama a una función de diseño basada en el alto de la cinta de opciones devuelto por el método [**IUIRibbon:: getHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , vea el [ejemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

En el ejemplo de código siguiente se muestra una implementación de [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementar un adaptador de IUICommandHandler

Dependiendo del diseño de la aplicación original, es posible que sea más fácil tener varias implementaciones de controlador de comandos o un solo controlador de comandos de puente que invoque la lógica de comandos de la aplicación existente. Muchas aplicaciones usan \_ mensajes de comandos de WM para este propósito en los que es suficiente proporcionar un controlador de comandos único y para todos los propósitos que simplemente reenvía \_ los mensajes de comandos de WM a la ventana de nivel superior.

Sin embargo, este enfoque requiere un tratamiento especial para comandos como **Exit** o **Close**. Dado que la cinta de opciones no se puede destruir mientras está procesando un mensaje de ventana, el \_ mensaje de cierre de WM debe publicarse en el subproceso de la interfaz de usuario de la aplicación y no debe procesarse sincrónicamente, como se muestra en el ejemplo siguiente:


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Migrar recursos

Una vez que se ha definido el manifiesto de comandos, se ha declarado la estructura de la cinta de opciones y el código de aplicación se ha adaptado para hospedar el marco de cinta, el último paso es la especificación de los recursos de cadena e imagen para cada comando.

> [!Note]  
> Los recursos de cadena e imagen se proporcionan normalmente en el archivo de marcado. Sin embargo, se pueden generar o reemplazar mediante programación implementando el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

 

### <a name="string-resources"></a>Recursos de cadena

[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) es la propiedad de cadena más común definida para un comando. Se representan como etiquetas de texto para pestañas, grupos y controles individuales. Normalmente, una cadena de etiqueta de un elemento de menú heredado se puede volver a usar para un **comando. LabelTitle** sin mucha edición.

Sin embargo, las siguientes convenciones han cambiado con la llegada de la cinta de opciones:

-   El sufijo de puntos suspensivos (...), que se usa para indicar un comando de inicio de diálogo, ya no es necesario.
-   El símbolo de y comercial (&) se puede seguir usando para indicar un método abreviado de teclado para un comando que aparece en un menú, pero la propiedad [**Command. KeyTip**](windowsribbon-element-command-keytip.md) compatible con el marco de trabajo cumple un propósito similar.

En el ejemplo de editor de texto, se pueden especificar las siguientes cadenas para LabelTitle y KeyTip:



| Símbolo           | Cadena original | Cadena LabelTitle | Cadena de KeyTip |
|------------------|-----------------|-------------------|---------------|
| archivo de ID. \_ \_ nuevo    | &nuevo            | &nuevo              | N             |
| archivo de identificador \_ \_ guardado   | &guardar           | &guardar             | S             |
| archivo de ID. \_ \_ guardado | Guardar &como...       | Guardar &como          | A             |
| IDENTIFICADOR de \_ archivo \_ abierto   | &abrir...          | &amp;Open             | O             |
| \_salida de archivo de identificador \_   | &Salir           | &Salir             | X             |
| deshacer edición de ID. \_ \_   | Deshacer &           | Deshacer              | Z             |
| \_cortar edición de ID. \_    | Cu&t            | Cu&t              | X             |
| \_editar la \_ copia de edición   | &copiar           | &copiar             | C             |
| \_pegar edición de ID. \_  | &pegar          | &pegar            | V             |
| \_borrado de edición de ID. \_  | &eliminar         | &eliminar           | D             |
| \_zoom de vista de identificador \_   | &zoom...          | Zoom              | Z             |



 

A continuación se muestra una lista de otras propiedades de cadena que se deben establecer en la mayoría de los comandos:

-   [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Ahora se pueden declarar pestañas, grupos y otras características de la interfaz de usuario de la cinta de opciones con todos los recursos de cadena e imagen especificados.

En el siguiente ejemplo de marcado de cinta se muestran varios recursos de cadena:


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Recursos de imagen

El marco de cinta admite formatos de imagen que proporcionan una apariencia mucho más enriquecida que los formatos de imagen admitidos por los componentes de menú y barra de herramientas anteriores.

En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.

En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.

> [!Note]  
> Los archivos de imagen existentes se pueden convertir a cualquier formato. Sin embargo, los resultados pueden ser menos satisfactorios si los archivos de imagen no admiten el suavizado de contorno y la transparencia.

 

No es posible especificar un tamaño predeterminado único para los recursos de imagen en el marco de la cinta de opciones. Sin embargo, para admitir el [diseño adaptable](windowsribbon-templates.md) de los controles, las imágenes se pueden especificar en dos tamaños (grande y pequeño). Todas las imágenes en el marco de cinta se escalan según la resolución de puntos por pulgada (PPP) de la pantalla con el tamaño representado exacto que depende de esta configuración de PPP. Consulte [especificar recursos de imagen de cinta](windowsribbon-imageformats.md) para obtener más información.

En el ejemplo siguiente se muestra cómo se hace referencia a un conjunto de imágenes específicas de PPP en el marcado:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar recursos de imagen de cinta](windowsribbon-imageformats.md)
</dt> </dl>

 

 