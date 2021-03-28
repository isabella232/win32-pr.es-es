---
description: La barra del explorador se incorporó con Microsoft Internet Explorer 4,0 para proporcionar un área de presentación adyacente al panel del explorador.
title: Creación de barras del explorador, bandas de herramientas y bandas de escritorio personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566395"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Crear barras del explorador personalizadas, bandas de herramientas y bandas del Departamento de soporte técnico

La barra del explorador se incorporó con Microsoft Internet Explorer 4,0 para proporcionar un área de presentación adyacente al panel del explorador. Básicamente es una ventana secundaria dentro de la ventana de Windows Internet Explorer y se puede usar para mostrar información e interactuar con el usuario de forma muy similar. Las barras del explorador se muestran normalmente como un panel vertical en el lado izquierdo del panel del explorador. Sin embargo, también se puede mostrar una barra del explorador horizontalmente, debajo del panel del explorador.

![Captura de pantalla que muestra las barras del explorador vertical y horizontal.](images/expl1.jpg)

Hay una amplia gama de usos posibles para la barra del explorador. Los usuarios pueden seleccionar la opción que desean ver de varias maneras diferentes, como seleccionarla en el submenú de la **barra del explorador** del menú **Ver** o hacer clic en un botón de la barra de herramientas. Internet Explorer proporciona varias barras del explorador estándar, como favoritos y búsqueda.

Una de las formas en que puede personalizar Internet Explorer es mediante la adición de una barra personalizada del explorador. Cuando se implementa y registra, se agrega al submenú de la **barra del explorador** del menú **Ver** . Cuando el usuario lo selecciona, se puede usar el área de presentación de la barra del explorador para mostrar información y tomar los datos proporcionados por el usuario de la misma manera que una ventana normal.

![captura de pantalla de las barras del explorador](images/expl2.jpg)

Para crear una barra personalizada del explorador, debe implementar y registrar un *objeto de banda*. Los objetos de banda se introdujeron con la versión 4,71 del shell y proporcionan funcionalidades similares a las de las ventanas normales. Sin embargo, dado que son objetos del modelo de objetos componentes (COM) y están contenidos en Internet Explorer o en el Shell, se implementan de forma ligeramente diferente. Los objetos de banda simple se usaron para crear las barras del explorador de ejemplo que se muestran en el primer gráfico. La implementación del ejemplo de la barra del explorador vertical se tratará en detalle en una sección posterior.

## <a name="tool-bands"></a>Bandas de herramientas

Una *banda de herramientas* es un objeto de banda incluido en Microsoft Internet Explorer 5 para admitir la característica de barra de herramientas de radio de Windows. La barra de herramientas de Internet Explorer es en realidad un [control rebar](../controls/rebar-controls.md) que contiene varios [controles de barra de herramientas](../controls/toolbar-control-reference.md). Al crear una banda de herramientas, puede Agregar una banda a ese control rebar. Sin embargo, al igual que las barras del explorador, una banda de herramientas es una ventana de uso general.

![captura de pantalla de bandas de herramientas](images/toolband1.jpg)

Los usuarios muestran una barra de herramientas seleccionándola en el submenú **barras de herramientas** del menú **Ver** o en el menú contextual que se muestra al hacer clic con el botón secundario en el área de la barra de herramientas.

## <a name="desk-bands"></a>Bandas del escritorio

Los objetos de banda también se pueden usar para crear *bandas del escritorio*. Aunque su implementación básica es similar a las barras del explorador, las bandas del escritorio no están relacionadas con Internet Explorer. Una banda de escritorio es básicamente una manera de crear una ventana acoplable en el escritorio. El usuario lo selecciona haciendo clic con el botón secundario en la barra de tareas y seleccionándolo en el submenú **barras de herramientas** .

![Captura de pantalla que muestra una banda de escritorio de ejemplo.](images/desk2.png)

Inicialmente, las bandas del escritorio se acoplan en la barra de tareas.

![Captura de pantalla que muestra las bandas de escritorio acopladas en la barra de tareas.](images/desk1.jpg)

A continuación, el usuario puede arrastrar la banda de escritorio al escritorio y aparecerá como una ventana normal.

![captura de pantalla de bandas de escritorio](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementar objetos de banda

Se tratan los temas siguientes.

-   [Aspectos básicos de los objetos de banda](#band-object-basics)
-   [Registro de banda](#band-registration)
-   [Un ejemplo sencillo de una barra del explorador personalizada](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Aspectos básicos de los objetos de banda

Aunque se pueden usar de forma muy parecida a las ventanas normales, los objetos de banda son objetos COM que existen dentro de un contenedor. Las barras del explorador están contenidas en Internet Explorer y las bandas del escritorio están contenidas en el shell. Aunque sirven diferentes funciones, su implementación básica es muy similar. La principal diferencia radica en cómo se registra el objeto de banda, que a su vez controla el tipo de objeto y su contenedor. En esta sección se describen los aspectos de implementación comunes a todos los objetos de banda. Vea [un ejemplo sencillo de una barra del explorador personalizada](#a-simple-example-of-a-custom-explorer-bar) para obtener más detalles sobre la implementación.

Además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), todos los objetos de banda deben implementar las interfaces siguientes.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Además de registrar su identificador de clase (CLSID), los objetos de la barra del explorador y de la banda del escritorio también deben estar registrados para la categoría del componente correspondiente. El registro de la categoría de componentes determina el tipo de objeto y su contenedor. Las bandas de herramientas usan un procedimiento de registro diferente y no tienen un identificador de categoría (CATId). Los CATID de los tres objetos de banda que los necesitan son:



| Tipo de banda               | Categoría de componentes |
|-------------------------|--------------------|
| Barra del explorador vertical   | CATId \_ InfoBand    |
| Barra del explorador horizontal | CATId \_ CommBand    |
| Banda de escritorio               | CATId \_ DeskBand    |



 

Consulte [registro de banda](#band-registration) para obtener más información sobre cómo registrar objetos de banda.

Si el objeto de banda va a aceptar la entrada del usuario, también debe implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Para agregar elementos al menú contextual de las bandas del escritorio o de la barra del explorador, el objeto de banda debe exportar [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Las bandas de herramientas no admiten menús contextuales.

Dado que los objetos de banda implementan una ventana secundaria, también deben implementar un procedimiento de ventana para controlar la mensajería de Windows.

Los objetos de banda pueden enviar comandos a su contenedor a través de la interfaz [**IOLECommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) del contenedor. Para obtener el puntero de interfaz, llame al método [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenedor y solicite IOLECOMMANDTARGET de IID \_ . Después, envía comandos al contenedor con [**IOLECommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). El grupo de comandos es CGID \_ DeskBand. Cuando se llama al método [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) de un objeto de banda, el contenedor usa el parámetro *dwBandID* para asignar el objeto de banda a un identificador que se usa para tres de los comandos. Se admiten cuatro identificadores de comando **IOLECommandTarget:: exec** .

-   DBID \_ BANDINFOCHANGED

    La información de la banda ha cambiado. Establezca el parámetro *pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). El contenedor llamará al método **IDeskBand:: GetBandInfo** del objeto de banda para solicitar la información actualizada.

-   DBID \_ MAXIMIZEBAND

    Maximice la banda. Establezca el parámetro *pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ SHOWONLY

    Activar o desactivar otras bandas del contenedor. Establezca el parámetro *pvaIn* en el \_ tipo desconocido de VT con uno de los siguientes valores:

    

    | Value | Descripción                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | pUnk  | Puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto de banda. Se ocultarán todas las demás bandas del escritorio. |
    | 0     | Ocultar todas las bandas del escritorio.                                                                                        |
    | 1     | Mostrar todas las bandas del escritorio.                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [Versión 5](versions.md). Mostrar un menú de botón de contenido adicional. El contenedor envía un mensaje [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) y el objeto Band recibe una notificación [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) que le pide que muestre el menú de comillas angulares. Establezca el parámetro *nCmdExecOpt* del método [**IOLECommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) en el identificador de banda recibido en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Establezca el parámetro *pvaIn* del método **IOLECommandTarget:: exec** en el tipo de la \_ aplicación VT con un valor definido por la aplicación. Vuelve a pasar al objeto de banda como el valor *lAppValue* de la \_ notificación CHEVRONPUSHED de RBN.

### <a name="band-registration"></a>Registro de banda

Un objeto de banda se debe registrar como un servidor de tipo OLE en proceso que admite el subprocesamiento de apartamento. El valor predeterminado del servidor es una cadena de texto de menú. En el caso de las barras del explorador, aparecerá en el submenú de la **barra del explorador** del menú **Ver** de Internet Explorer. En el caso de las bandas de herramientas, aparecerá en el submenú **barras de herramientas** del menú **Ver** de Internet Explorer. En el caso de las bandas del escritorio, aparecerá en el submenú **barras de herramientas** del menú contextual de la barra de tareas. Al igual que con los recursos de menú, si coloca una y comercial (&) delante de una letra, se subrayará y se habilitarán los métodos abreviados de teclado. Por ejemplo, la cadena de menú de la barra del explorador vertical que se muestra en el primer gráfico es "ejemplo &barra del explorador vertical".

Inicialmente, Internet Explorer recupera una enumeración de los objetos de barra del explorador registrados del registro mediante las categorías de componentes. Para aumentar el rendimiento, almacena en caché esta enumeración, lo que provoca que se pasen por alto las barras del explorador agregadas posteriormente. Para forzar a Windows Internet Explorer a volver a generar la memoria caché y reconocer una nueva barra del explorador, elimine las siguientes claves del registro durante el registro de la nueva barra del explorador:

**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **descartable** \\ **postsetup** \\ **Component Categories** \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**

**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **descartable** \\ **postsetup** \\ **Component Categories** \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**

> [!Note]  
> Dado que se crea una memoria caché de la barra del explorador para cada usuario, es posible que la aplicación de instalación tenga que enumerar todos los subárboles del registro del usuario o agregar un código auxiliar por usuario para que se ejecute cuando el usuario inicie sesión por primera vez.

 

En general, la entrada básica del registro para un objeto de banda aparecerá de la siguiente manera.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Los grupos de herramientas también deben tener el CLSID del objeto registrado con Internet Explorer. Para ello, asigne un valor en la barra de herramientas **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\  denominada con el GUID de CLSID del objeto de banda de herramientas, como se muestra aquí. Se omite su valor de datos, por lo que el tipo de valor no es importante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Hay varios valores opcionales que también se pueden agregar al registro. Por ejemplo, el siguiente valor es necesario si desea usar la barra del explorador para mostrar el código HTML; el valor que se muestra no es un ejemplo, sino el valor real que se debe usar.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Cuando se usa junto con el valor mostrado anteriormente, también es necesario el siguiente valor opcional si desea utilizar la barra del explorador para mostrar el código HTML. Este valor debe establecerse en la ubicación del archivo que contiene el contenido HTML de la barra del explorador.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Otro valor opcional define el ancho o el alto predeterminados de la barra del explorador, en función de si es vertical u horizontal, respectivamente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

El valor de UpBars debe establecerse en el ancho o el alto de la barra. El valor requiere ocho bytes y se coloca en el registro como un valor binario. Los primeros cuatro bytes especifican el tamaño en píxeles, en formato hexadecimal, empezando por el byte más a la izquierda. Los últimos cuatro bytes están reservados y deben establecerse en cero.

Por ejemplo, aquí se muestran las entradas del registro completas para una barra del explorador compatible con HTML con un ancho predeterminado de 291 píxeles (0x123).

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

Puede controlar el registro del CATId de un objeto de banda mediante programación. Cree un objeto de administrador de categorías de componentes (CLSID \_ StdComponentCategoriesMgr) y solicite un puntero a su interfaz [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) . Pase el CLSID del objeto de banda y el CATId a [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Un ejemplo sencillo de una barra del explorador personalizada

Este ejemplo pasa por la implementación de la barra del explorador vertical de ejemplo que se muestra en la introducción.

El procedimiento básico para crear una barra personalizada del explorador es el siguiente.

1.  [Implemente las funciones necesarias para la dll](#dll-functions).
2.  [Implemente las interfaces COM necesarias.](#required-interface-implementations)
3.  [Implemente las interfaces COM opcionales que desee.](#optional-interface-implementations)
4.  [Registre el CLSID del objeto y, si es necesario, la categoría de componente.](#clsid-registration)
5.  Cree una ventana secundaria de Internet Explorer cuyo tamaño se ajuste a la región de visualización de la barra del explorador.
6.  [Use la ventana secundaria para mostrar información e interactuar con el usuario.](#the-window-procedure)

La implementación muy sencilla que se usa en el ejemplo de la barra del explorador se podría usar realmente para cualquier tipo de barra del explorador, o una banda de escritorio, simplemente registrándose en la categoría del componente correspondiente. Las implementaciones más sofisticadas deberán personalizarse para la región y el contenedor de visualización de cada tipo de objeto. Sin embargo, gran parte de esta personalización se puede llevar a cabo mediante el uso del código de ejemplo y su extensión aplicando técnicas de programación de Windows conocidas a la ventana secundaria. Por ejemplo, puede Agregar controles para la interacción del usuario o gráficos para una pantalla más completa.

### <a name="dll-functions"></a>Funciones DLL

Los tres objetos se empaquetan en un solo archivo DLL, que expone las siguientes funciones.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Las tres primeras funciones son implementaciones estándar y no se tratarán aquí. La implementación del generador de clases también es estándar.

### <a name="required-interface-implementations"></a>Implementaciones de interfaz necesarias

El ejemplo de barra del explorador vertical implementa las cuatro interfaces necesarias: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)y [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) como parte de la clase CExplorerBar. Las implementaciones de constructor, destructor e **IUnknown** son sencillas y no se tratarán aquí. Vea el código de ejemplo para obtener más detalles.

Las siguientes interfaces se describen en detalle.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Cuando el usuario selecciona una barra del explorador, el contenedor llama al método [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) del objeto de banda correspondiente. El parámetro *punkSite* se establecerá en el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sitio.

En general, una implementación de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) debe realizar los siguientes pasos:

1.  Libera todos los punteros de sitio que se están conservando actualmente.
2.  Si el puntero que se pasa a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) se establece en **null**, se quita la banda. **SetSite** puede devolver S \_ correcto.
3.  Si el puntero que se pasa a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no es **null**, se establece un nuevo sitio. **SetSite** debe hacer lo siguiente:
    1.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su interfaz [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .
    2.  Llame a [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para obtener el identificador de la ventana primaria. Guarde el identificador para su uso posterior. Libere [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) si ya no es necesario.
    3.  Cree la ventana del objeto de banda como un elemento secundario de la ventana obtenida en el paso anterior. No lo cree como una ventana visible.
    4.  Si el objeto Band implementa [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su interfaz [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) . Almacene el puntero en esta interfaz para su uso posterior.
    5.  Si todos los pasos se realizan correctamente, vuelva a ser correcto \_ . En caso contrario, devuelve el código de error definido por OLE que indica el error.

El ejemplo de barra del explorador implementa [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) de la siguiente manera. En el siguiente código *m \_ pSite* es una variable miembro privada que contiene el puntero [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y *m \_ hwndParent* contiene el identificador de la ventana primaria. En este ejemplo, también se controla la creación de ventanas. Si la ventana no existe, este método crea la ventana de la barra del explorador como un elemento secundario con el tamaño adecuado de la ventana primaria obtenida por **SetSite**. El identificador de la ventana secundaria se almacena en *m \_ hWnd*.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



La implementación de [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) del ejemplo simplemente ajusta una llamada al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sitio mediante el puntero de sitio guardado por [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer llamará a la interfaz [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) de la barra del explorador para permitir que la barra del explorador cargue o guarde datos persistentes. Si no hay datos persistentes, los métodos deben devolver un código de éxito. La interfaz **IPersistStream** hereda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), por lo que deben implementarse cinco métodos.

-   [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream:: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream:: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream:: GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

El ejemplo de barra del explorador no usa ningún dato persistente y solo tiene una implementación mínima de [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) devuelve el CLSID del objeto (CLSID \_ SampleExplorerBar) y el resto devuelven los valores \_ correcto, s \_ false o E \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

La interfaz [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) es específica de los objetos de banda. Además de su método, hereda de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), que a su vez hereda de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Hay dos métodos [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) y [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). La implementación del ejemplo de barra del explorador de **GetWindow** devuelve el identificador de la ventana secundaria de la barra del explorador, *m \_ hWnd*. No se ha implementado la ayuda contextual, por lo que **ContextSensitiveHelp** devuelve **E \_ NOTIMPL**.

La interfaz [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) tiene tres métodos.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

El método [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) no se usa con ningún tipo de objeto de banda y siempre debe devolver E \_ NOTIMPL. El método [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) muestra u oculta la ventana de la barra del explorador, dependiendo del valor de su parámetro.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



El método [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) destruye la ventana de la barra del explorador.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



El método restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), es específico de **IDeskBand**. Internet Explorer lo utiliza para especificar el identificador y el modo de visualización de la barra del explorador. Internet Explorer también puede solicitar uno o más datos de la barra del explorador rellenando el miembro **dwMask** de la estructura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) que se pasa como tercer parámetro. **GetBandInfo** debe almacenar el identificador y el modo de visualización y rellenar la estructura **DESKBANDINFO** con los datos solicitados. El ejemplo de barra del explorador implementa **GetBandInfo** como se muestra en el ejemplo de código siguiente.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Implementaciones de interfaz opcionales

Hay dos interfaces que no son necesarias, pero que pueden ser útiles para implementar: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) y [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). El ejemplo de barra del explorador implementa **IInputObject**. Consulte la documentación para obtener información sobre cómo implementar **IContextMenu**.

### <a name="iinputobject"></a>IInputObject

La interfaz [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) debe implementarse si un objeto de banda acepta datos proporcionados por el usuario. Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y usa **IInputObject** para mantener el foco de entrada del usuario adecuado cuando tiene más de una ventana contenida. Hay tres métodos que deben implementarse en una barra del explorador.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer llama a [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) para informar a la barra del explorador de que se está activando o desactivando. Cuando se activa, el ejemplo de la barra del explorador llama a [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) para establecer el foco en su ventana.

Internet Explorer llama a [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) cuando intenta determinar qué ventana tiene el foco. Si la ventana de la barra del explorador o uno de sus descendientes tiene el foco, **HasFocusIO** debe devolver s \_ correcto. Si no es así, debe devolver S \_ false.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permite al objeto procesar aceleradores de teclado. El ejemplo de barra del explorador no implementa este método, por lo que devuelve S \_ false.

La implementación de la barra de ejemplo de [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) es la siguiente.


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>Registro de CLSID

Al igual que con todos los objetos COM, se debe registrar el CLSID de la barra del explorador. Para que el objeto funcione correctamente con Internet Explorer, también debe estar registrado para la categoría de componente correspondiente (CATId \_ InfoBand). En el ejemplo de código siguiente se muestra la sección de código correspondiente de la barra del explorador.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



El registro de objetos de banda en el ejemplo utiliza procedimientos COM normales.

Además del CLSID, el servidor de objetos de banda también debe estar registrado para una o varias categorías de componentes. Esta es realmente la diferencia principal de la implementación entre los ejemplos de barras del explorador vertical y horizontal. Para controlar este proceso, se crea un objeto de administrador de categorías de componentes (CLSID \_ StdComponentCategoriesMgr) y se usa el método [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) para registrar el servidor de objetos de banda. En este ejemplo, el registro de categoría de componente se controla pasando el CLSID y el CATId de la barra del explorador a una función privada (**RegisterComCat**) como se muestra en el ejemplo de código siguiente.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>El procedimiento de ventana

Dado que un objeto de banda usa una ventana secundaria para su presentación, debe implementar un procedimiento de ventana para controlar la mensajería de Windows. El ejemplo de banda tiene una funcionalidad mínima, por lo que su procedimiento de ventana solo controla cinco mensajes:

-   [**NCCREATE de WM \_**](../winmsg/wm-nccreate.md)
-   [**pintura de WM \_**](../gdi/wm-paint.md)
-   [**comando de WM \_**](../menurc/wm-command.md)
-   [**SETFOCUS de WM \_**](../inputdev/wm-setfocus.md)
-   [**KILLFOCUS de WM \_**](../inputdev/wm-killfocus.md)

El procedimiento se puede expandir fácilmente para dar cabida a otros mensajes para admitir más características.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



El controlador de comandos de WM \_ simplemente devuelve cero. El controlador de pintura de WM \_ crea la presentación de texto simple que se muestra en el ejemplo de la barra del explorador en la introducción.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



Los \_ controladores de WM SETFOCUS y WM \_ KILLFOCUS informan al sitio de un cambio de foco llamando al método [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) del sitio.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Los objetos de banda proporcionan una forma flexible y eficaz de ampliar las capacidades de Internet Explorer mediante la creación de barras personalizadas del explorador. La implementación de una banda de escritorio le permite ampliar las capacidades de las ventanas normales. Aunque se requiere cierta programación COM, en última instancia sirve para proporcionar una ventana secundaria para la interfaz de usuario. A partir de ahí, la mayor parte de la implementación puede usar técnicas de programación de Windows conocidas. Aunque el ejemplo que se describe aquí solo tiene una funcionalidad limitada, ilustra todas las características necesarias de un objeto de banda y se puede ampliar fácilmente para crear una interfaz de usuario única y eficaz.

 

 
