---
description: La barra del explorador se introdujo con Microsoft Internet Explorer 4.0 para proporcionar un área de presentación adyacente al panel del explorador.
title: Creación de barras del explorador, bandas de herramientas y bandas de escritorio personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9a57cc5bc8afa3e973c6d4d99b8bcee186287a6c9278407b900f84500d7d0e51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461746"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Crear barras de explorador personalizadas, bandas de herramientas y bandas de escritorio

La barra del explorador se introdujo con Microsoft Internet Explorer 4.0 para proporcionar un área de presentación adyacente al panel del explorador. Básicamente, es una ventana secundaria dentro de la ventana Windows Internet Explorer y se puede usar para mostrar información e interactuar con el usuario de la misma manera. Las barras del explorador se muestran normalmente como un panel vertical en el lado izquierdo del panel del explorador. Sin embargo, una barra del explorador también se puede mostrar horizontalmente, debajo del panel del explorador.

![Captura de pantalla que muestra las barras del explorador vertical y horizontal.](images/expl1.jpg)

Hay una amplia gama de posibles usos para la barra del explorador. Los usuarios pueden seleccionar qué opción quieren ver de varias maneras diferentes,  como seleccionarla en el **submenú** Barra del explorador del menú Ver o hacer clic en un botón de la barra de herramientas. Internet Explorer proporciona varias barras estándar del Explorador, como Favoritos y Búsqueda.

Una de las formas de personalizar el Internet Explorer es agregar una barra de explorador personalizada. Cuando se implemente y registre, se agregará al submenú **Barra** del explorador del **menú** Ver. Cuando el usuario lo selecciona, el área de presentación de la barra del explorador se puede usar para mostrar información y tomar la entrada del usuario de la misma manera que una ventana normal.

![captura de pantalla de las barras del explorador](images/expl2.jpg)

Para crear una barra de explorador personalizada, debe implementar y registrar un objeto *de banda*. Los objetos de banda se introdujeron con la versión 4.71 del Shell y proporcionan funcionalidades similares a las de las ventanas normales. Sin embargo, dado que son objetos del Modelo de objetos componentes (COM) y están incluidos en Internet Explorer o shell, se implementan de forma ligeramente diferente. Los objetos de banda simple se usaron para crear las barras del explorador de ejemplo que se muestran en el primer gráfico. La implementación del ejemplo de barra del explorador vertical se analizará en detalle en una sección posterior.

## <a name="tool-bands"></a>Bandas de herramientas

Una *banda de herramientas* es un objeto de banda que se introdujo con Microsoft Internet Explorer 5 para admitir la característica Windows barra de herramientas de radio. La Internet Explorer barra de herramientas es realmente un [control rebar](../controls/rebar-controls.md) que contiene varios controles [de barra de herramientas](../controls/toolbar-control-reference.md). Al crear una banda de herramientas, puede agregar una banda a ese control rebar. Sin embargo, al igual que las barras del explorador, una banda de herramientas es una ventana de uso general.

![captura de pantalla de bandas de herramientas](images/toolband1.jpg)

Los usuarios muestran una barra de herramientas seleccionándose  en el **submenú** Barras de herramientas del menú Ver o en el menú contextual que se muestra haciendo clic con el botón derecho en el área de la barra de herramientas.

## <a name="desk-bands"></a>Bandas de escritorio

Los objetos de banda también se pueden usar para crear bandas *de escritorio.* Aunque su implementación básica es similar a las barras del explorador, las bandas de escritorio no están relacionadas con Internet Explorer. Una banda de escritorio es básicamente una manera de crear una ventana acoplable en el escritorio. El usuario lo selecciona haciendo clic con el botón derecho en la barra de tareas y seleccionándose en el **submenú Barras de** herramientas.

![Captura de pantalla que muestra una banda de escritorio de ejemplo.](images/desk2.png)

Inicialmente, las bandas de escritorio se acoplan en la barra de tareas.

![Captura de pantalla que muestra bandas de escritorio acopladas en la barra de tareas.](images/desk1.jpg)

A continuación, el usuario puede arrastrar la banda de escritorio al escritorio y aparecerá como una ventana normal.

![captura de pantalla de bandas de escritorio](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementar objetos de banda

Se tratan los temas siguientes.

-   [Aspectos básicos de los objetos de banda](#band-object-basics)
-   [Registro de banda](#band-registration)
-   [Un ejemplo sencillo de una barra de Explorador personalizado](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Aspectos básicos de los objetos de banda

Aunque se pueden usar de forma muy parecido a las ventanas normales, los objetos de banda son objetos COM que existen dentro de un contenedor. Las barras del explorador están contenidas en Internet Explorer, y las bandas de escritorio están contenidas en el shell. Aunque sirven funciones diferentes, su implementación básica es muy similar. La diferencia principal radica en cómo se registra el objeto de banda, que a su vez controla el tipo de objeto y su contenedor. En esta sección se de abordan los aspectos de implementación que son comunes a todos los objetos de banda. Vea [Un ejemplo sencillo de una barra de explorador personalizado para](#a-simple-example-of-a-custom-explorer-bar) obtener más detalles de implementación.

Además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)todos los objetos de banda deben implementar las interfaces siguientes.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**Ipersiststream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Además de registrar su identificador de clase (CLSID), también se deben registrar los objetos de barra del explorador y de banda de escritorio para la categoría de componente adecuada. El registro de la categoría de componentes determina el tipo de objeto y su contenedor. Las bandas de herramientas usan un procedimiento de registro diferente y no tienen un identificador de categoría (CATID). Los CATID de los tres objetos de banda que los requieren son:



| Tipo de banda               | Categoría de componentes |
|-------------------------|--------------------|
| Barra del explorador vertical   | CATID \_ InfoBand    |
| Barra del Explorador horizontal | CATID \_ CommBand    |
| Banda de escritorio               | CATID \_ DeskBand    |



 

Consulte [Registro de banda para](#band-registration) obtener más información sobre cómo registrar objetos de banda.

Si el objeto de banda va a aceptar la entrada del usuario, también debe implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Para agregar elementos al menú contextual de barras del explorador o bandas de escritorio, el objeto de banda debe exportar [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Las bandas de herramientas no admiten menús contextuales.

Dado que los objetos de banda implementan una ventana secundaria, también deben implementar un procedimiento de ventana para controlar Windows mensajería.

Los objetos de banda pueden enviar comandos a su contenedor a través de la [**interfaz IOleCommandTarget del**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) contenedor. Para obtener el puntero de interfaz, llame al método [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenedor y solicite IID \_ IOleCommandTarget. A continuación, envíe comandos al contenedor [**con IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). El grupo de comandos es CGID \_ DeskBand. Cuando se llama al método [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) de un objeto de banda, el contenedor usa el parámetro *dwBandID* para asignar al objeto de banda un identificador que se usa para tres de los comandos. Se **admiten cuatro IOleCommandTarget::Exec.**

-   DBID \_ BANDINFOCHANGED

    La información de la banda ha cambiado. Establezca el *parámetro pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). El contenedor llamará al método **IDeskBand::GetBandInfo** del objeto de banda para solicitar la información actualizada.

-   DBID \_ MAXIMIZEBAND

    Maximice la banda. Establezca el *parámetro pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ SHOWONLY

    Active o desactive otras bandas del contenedor. Establezca el *parámetro pvaIn* en el tipo \_ VT UNKNOWN con uno de los valores siguientes:

    

    | Valor | Descripción                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | Punk  | Puntero a la interfaz [**IUnknown del objeto de**](/windows/win32/api/unknwn/nn-unknwn-iunknown) banda. Todas las demás bandas de escritorio estarán ocultas. |
    | 0     | Ocultar todas las bandas de escritorio.                                                                                        |
    | 1     | Mostrar todas las bandas de escritorio.                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [Versión 5.](versions.md) Muestra un menú de contenido adicional. El contenedor envía un mensaje [**\_ PUSHCHEVRON**](../controls/rb-pushchevron.md) de RB y el objeto de banda recibe una notificación [ \_ RBN CHEVRONPUSHED](../controls/rbn-chevronpushed.md) que le pide que muestre el menú de contenido adicional. Establezca el parámetro *nCmdExecOpt* del método [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) en el identificador de banda recibido en la llamada más reciente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Establezca el parámetro *pvaIn* del método **IOleCommandTarget::Exec** en el tipo VT I4 con un \_ valor definido por la aplicación. Se pasa de nuevo al objeto de banda como el *valor lAppValue* de la notificación \_ RBN CHEVRONPUSHED.

### <a name="band-registration"></a>Registro de banda

Un objeto de banda se debe registrar como un servidor OLE en proceso que admita subprocesos de contenedor. El valor predeterminado del servidor es una cadena de texto de menú. En el caso de las barras del explorador, aparecerá en el submenú **Barra** del explorador Internet Explorer **menú** Ver. En el caso de las bandas de herramientas, aparecerá en el submenú Barras de **herramientas** del Internet Explorer **menú** Ver. En el caso de las bandas de escritorio, aparecerá en el submenú Barras de **herramientas** del menú contextual de la barra de tareas. Al igual que con los recursos de menú, colocar una yand (&) delante de una letra hará que se subrayado y se habiliten los métodos abreviados de teclado. Por ejemplo, la cadena de menú de la barra de explorador vertical que se muestra en el primer gráfico es "Sample &Vertical Explorer Bar".

Inicialmente, Internet Explorer recupera una enumeración de los objetos de barra del explorador registrados del registro mediante las categorías de componentes. Para aumentar el rendimiento, almacena en caché esta enumeración, lo que hace que se pasen por alto las barras del explorador agregadas posteriormente. Para forzar Windows Internet Explorer recompilar la memoria caché y reconocer una nueva barra del Explorador, elimine las siguientes claves del Registro durante el registro de la nueva barra del explorador:

**HKEY \_ Current \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021493-0000-0000-C000-000000000046}** \\ **Enum**

**HKEY \_ Current \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021494-0000-0000-C000-000000000046}** \\ **Enum**

> [!Note]  
> Dado que se crea una memoria caché de la barra del explorador para cada usuario, es posible que la aplicación de instalación tenga que enumerar todos los subárboles del Registro de usuarios o agregar un código auxiliar por usuario para que se ejecute cuando el usuario inicie sesión por primera vez.

 

En general, la entrada básica del Registro para un objeto de banda aparecerá como se muestra a continuación.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Las bandas de herramientas también deben tener el CLSID de su objeto registrado con Internet Explorer. Para ello, asigne un valor en **HKEY \_ LOCAL \_ MACHINE** Software Microsoft Internet Explorer Toolbar denominado con el GUID de \\  \\  \\  \\  CLSID del objeto de banda de herramientas, como se muestra aquí. Su valor de datos se omite, por lo que el tipo de valor no es importante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Hay varios valores opcionales que también se pueden agregar al Registro. Por ejemplo, el siguiente valor es necesario si desea usar la barra del explorador para mostrar HTML. El valor que se muestra no es un ejemplo, sino el valor real que se debe usar.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Se usa junto con el valor mostrado anteriormente, también es necesario el siguiente valor opcional si desea usar la barra del explorador para mostrar HTML. Este valor debe establecerse en la ubicación del archivo que contiene el contenido HTML de la barra del explorador.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Otro valor opcional define el ancho o alto predeterminados de la barra del explorador, dependiendo de si es vertical u horizontal, respectivamente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

El valor BarSize debe establecerse en el ancho o alto de la barra. El valor requiere ocho bytes y se coloca en el Registro como un valor binario. Los cuatro primeros bytes especifican el tamaño en píxeles, en formato hexadecimal, empezando por el byte situado más a la izquierda. Los últimos cuatro bytes están reservados y deben establecerse en cero.

Por ejemplo, las entradas del Registro completa para una barra de explorador compatible con HTML con un ancho predeterminado de 291 píxeles (0x123) se muestran aquí.

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

Puede controlar el registro del CATID de un objeto de banda mediante programación. Cree un objeto de administrador de categorías de componentes (CLSID \_ StdComponentCategoriesMgr) y solicite un puntero a su [**interfaz ICatRegister.**](/windows/win32/api/comcat/nn-comcat-icatregister) Pase el CLSID y el CATID del objeto de banda a [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Un ejemplo sencillo de una barra de explorador personalizado

En este ejemplo se pasa por la implementación de la barra de explorador vertical de ejemplo que se muestra en la introducción.

El procedimiento básico para crear una barra de explorador personalizada es el siguiente.

1.  [Implemente las funciones necesarias para el archivo DLL.](#dll-functions)
2.  [Implemente las interfaces COM necesarias.](#required-interface-implementations)
3.  [Implemente las interfaces COM opcionales deseadas.](#optional-interface-implementations)
4.  [Registre el CLSID del objeto y, si es necesario, la categoría de componente.](#clsid-registration)
5.  Cree una ventana secundaria de Internet Explorer tamaño que se ajuste a la región de presentación de la barra del explorador.
6.  [Use la ventana secundaria para mostrar información e interactuar con el usuario.](#the-window-procedure)

La implementación muy sencilla que se usa en el ejemplo de barra del explorador podría usarse realmente para cualquier tipo de barra del explorador o una banda de escritorio, simplemente registrándose para la categoría de componente adecuada. Es necesario personalizar implementaciones más sofisticadas para la región de presentación y el contenedor de cada tipo de objeto. Sin embargo, gran parte de esta personalización se puede realizar tomando el código de ejemplo y extendiendolo mediante la aplicación de técnicas de programación Windows a la ventana secundaria. Por ejemplo, puede agregar controles para la interacción del usuario o gráficos para una presentación más enriquección.

### <a name="dll-functions"></a>Funciones DLL

Los tres objetos se empaquetan en un único archivo DLL, que expone las siguientes funciones.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Las tres primeras funciones son implementaciones estándar y no se tratarán aquí. La implementación del generador de clases también es estándar.

### <a name="required-interface-implementations"></a>Implementaciones de interfaz requeridas

El ejemplo de barra del explorador vertical implementa las cuatro interfaces necesarias: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) como parte de la clase CExplorerBar. Las implementaciones de constructor, destructor e **IUnknown** son sencillas y no se tratarán aquí. Vea el código de ejemplo para obtener más detalles.

Las interfaces siguientes se de abordan en detalle.

-   [IObjectWithSite](#iobjectwithsite)
-   [Ipersiststream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Cuando el usuario selecciona una barra del explorador, el contenedor llama al método [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) del objeto de banda correspondiente. El *parámetro fuesite* se establecerá en el puntero [**IUnknown del**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sitio.

En general, una [**implementación de SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) debe realizar los pasos siguientes:

1.  Libere cualquier puntero de sitio que se esté retenido actualmente.
2.  Si el puntero pasado a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) se establece en **NULL,** se quita la banda. **SetSite** puede devolver S \_ OK.
3.  Si el puntero pasado a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no es **NULL,** se establece un nuevo sitio. **SetSite** debe hacer lo siguiente:
    1.  Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su [**interfaz IOleWindow.**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
    2.  Llame [**a IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para obtener el identificador de la ventana primaria. Guarde el identificador para su uso posterior. Libere [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) si ya no es necesario.
    3.  Cree la ventana del objeto de banda como elemento secundario de la ventana obtenida en el paso anterior. No lo cree como una ventana visible.
    4.  Si el objeto de banda implementa [**IInputObject,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su [**interfaz IInputObjectSite.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) Almacene el puntero a esta interfaz para usarlo más adelante.
    5.  Si todos los pasos se han realizado correctamente, devuelva S \_ OK. Si no es así, devuelva el código de error definido por OLE que indica el error.

El ejemplo de barra del explorador [**implementa SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) de la siguiente manera. En el código *siguiente, m \_ pSite* es una variable miembro privada que contiene el puntero [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y *m \_ hwndParent* contiene el identificador de la ventana primaria. En este ejemplo, también se controla la creación de ventanas. Si la ventana no existe, este método crea la ventana de la barra del explorador como un elemento secundario con el tamaño adecuado de la ventana primaria obtenida por **SetSite**. El identificador de la ventana secundaria se almacena en *m \_ hwnd*.


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



La implementación [**getSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) del ejemplo simplemente encapsula una llamada al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sitio, mediante el puntero de sitio guardado [**por SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


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



### <a name="ipersiststream"></a>Ipersiststream

Internet Explorer llamará a la interfaz [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) de la barra del explorador para permitir que la barra del explorador cargue o guarde datos persistentes. Si no hay datos persistentes, los métodos deben devolver un código correcto. La **interfaz IPersistStream** hereda de [**IPersist,**](/windows/win32/api/objidl/nn-objidl-ipersist)por lo que se deben implementar cinco métodos.

-   [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream::IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream::Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream::GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

El ejemplo de barra del explorador no usa ningún dato persistente y solo tiene una implementación mínima de [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) devuelve el CLSID del objeto (CLSID SampleExplorerBar) y el resto devuelve S OK, S FALSE o \_ E \_ \_ \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

La [**interfaz IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) es específica de los objetos de banda. Además de su único método, hereda de [**IDockingWindow,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)que a su vez hereda de [**IOleWindow.**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)

Hay dos métodos [**de IOleWindow:**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) [**e IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). La implementación del ejemplo de barra del explorador **de GetWindow** devuelve el identificador de ventana secundaria de la barra del explorador, *m \_ hwnd*. La Ayuda contextual no se implementa, por lo **que ContextSensitiveHelp** devuelve **E \_ NOTIMPL**.

La [**interfaz IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) tiene tres métodos.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

El [**método ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) no se usa con ningún tipo de objeto de banda y siempre debe devolver E \_ NOTIMPL. El [**método ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) muestra u oculta la ventana de la barra del explorador, en función del valor de su parámetro.


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



El [**método CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) destruye la ventana de la barra del explorador.


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



El método restante, [**GetBandInfo,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)es específico de **IDeskBand.** Internet Explorer usa para especificar el identificador y el modo de visualización de la barra del explorador. Internet Explorer puede solicitar uno o varios fragmentos de información de la barra del explorador rellenando el **miembro dwMask** de la estructura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) que se pasa como tercer parámetro. **GetBandInfo debe** almacenar el identificador y el modo de visualización y rellenar la **estructura DESKBANDINFO** con los datos solicitados. El ejemplo de barra del explorador **implementa GetBandInfo** como se muestra en el ejemplo de código siguiente.


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

Hay dos interfaces que no son necesarias, pero que pueden ser útiles para implementar: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). El ejemplo de barra del explorador implementa **IInputObject**. Consulte la documentación para obtener información sobre cómo implementar **IContextMenu**.

### <a name="iinputobject"></a>IInputObject

La [**interfaz IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) debe implementarse si un objeto de banda acepta la entrada del usuario. Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y usa **IInputObject** para mantener el foco de entrada del usuario adecuado cuando tiene más de una ventana independiente. Hay tres métodos que deben implementarse mediante una barra del explorador.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer llama a [**UIActivateIO para**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) informar a la barra del explorador de que se está activando o desactivando. Cuando se activa, el ejemplo de barra del explorador llama [**a SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) para establecer el foco en su ventana.

Internet Explorer llama [**a HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) cuando intenta determinar qué ventana tiene el foco. Si la ventana de la barra del explorador o uno de sus descendientes tiene el foco, **HasFocusIO** debe devolver S \_ OK. Si no es así, debe devolver S \_ FALSE.

[**TranslateAcceleratorIO permite**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) que el objeto procese los aceleradores de teclado. El ejemplo de barra del explorador no implementa este método, por lo que devuelve S \_ FALSE.

La implementación de [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) de la barra de ejemplo es la siguiente.


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

Al igual que con todos los objetos COM, se debe registrar el CLSID de la barra del explorador. Para que el objeto funcione correctamente con Internet Explorer, también se debe registrar para la categoría de componente adecuada (CATID \_ InfoBand). La sección de código correspondiente para la barra del explorador se muestra en el ejemplo de código siguiente.


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



El registro de objetos de banda en el ejemplo usa procedimientos COM normales.

Además del CLSID, el servidor de objetos de banda también debe registrarse para una o varias categorías de componentes. En realidad, esta es la principal diferencia en la implementación entre los ejemplos de barra del explorador vertical y horizontal. Este proceso se controla mediante la creación de un objeto de administrador de categorías de componentes (CLSID StdComponentCategoriesMgr) y el uso del método \_ [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) para registrar el servidor de objetos de banda. En este ejemplo, el registro de categorías de componentes se controla pasando el CLSID y CATID del ejemplo de barra del explorador a una función **privada, RegisterComCat,** como se muestra en el ejemplo de código siguiente.


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



### <a name="the-window-procedure"></a>Procedimiento de ventana

Dado que un objeto de banda usa una ventana secundaria para su presentación, debe implementar un procedimiento de ventana para controlar Windows mensajes. El ejemplo de banda tiene una funcionalidad mínima, por lo que su procedimiento de ventana solo controla cinco mensajes:

-   [**WM \_ NCCREATE**](../winmsg/wm-nccreate.md)
-   [**WM \_ PAINT**](../gdi/wm-paint.md)
-   [**COMANDO \_ WM**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**WM \_ KILLFOCUS**](../inputdev/wm-killfocus.md)

El procedimiento se puede expandir fácilmente para dar cabida a mensajes adicionales para admitir más características.


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



El controlador \_ WM COMMAND simplemente devuelve cero. El controlador \_ WM PAINT crea la presentación de texto simple que se muestra en el ejemplo de barra del explorador en la introducción.


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



Los controladores WM SETFOCUS y WM KILLFOCUS informan al sitio de un cambio de foco mediante una llamada al método \_ \_ [**IInputObjectSite::OnFocusChangeIS del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) sitio.


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



Los objetos de banda proporcionan una manera flexible y eficaz de ampliar las funcionalidades de Internet Explorer mediante la creación de barras de explorador personalizadas. La implementación de una banda de escritorio le permite ampliar las funcionalidades de las ventanas normales. Aunque se requiere alguna programación COM, en última instancia sirve para proporcionar una ventana secundaria para la interfaz de usuario. A partir de ahí, la mayor parte de la implementación puede usar técnicas Windows programación. Aunque el ejemplo que se describe aquí solo tiene una funcionalidad limitada, muestra todas las características necesarias de un objeto de banda y se puede ampliar fácilmente para crear una interfaz de usuario única y eficaz.

 

 
