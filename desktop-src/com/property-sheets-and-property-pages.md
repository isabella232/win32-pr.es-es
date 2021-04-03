---
title: Hojas de propiedades y páginas de propiedades
description: Hojas de propiedades y páginas de propiedades
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cc61d1e1ed0cb833632b6b627a0c683a3cb0e4
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "103913937"
---
# <a name="property-sheets-and-property-pages"></a>Hojas de propiedades y páginas de propiedades

Las propiedades de un objeto se exponen a los clientes de la misma forma que a los métodos a través de interfaces COM o de la implementación **IDispatch** del objeto, lo que permite que los programas cambien las propiedades que llaman a estos métodos. La tecnología OLE de las páginas de propiedades proporciona los medios para compilar una interfaz de usuario para las propiedades de un objeto de acuerdo con los estándares de la interfaz de usuario de Windows. Por lo tanto, las propiedades se exponen a los usuarios finales. La hoja de propiedades de un objeto es un cuadro de diálogo con pestañas donde cada pestaña corresponde a una página de propiedades concreta. El modelo OLE para trabajar con páginas de propiedades consta de estas características:

-   Cada página de propiedades se administra mediante un objeto en proceso que implementa [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) o [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2). Cada página se identifica con su propio CLSID único.
-   Un objeto especifica su compatibilidad con las páginas de propiedades implementando [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). A través de esta interfaz, el llamador puede obtener una lista de CLSID que identifiquen las páginas de propiedades específicas que admite el objeto. Si el objeto especifica el CLSID de una página de propiedades, el objeto debe ser capaz de recibir los cambios de propiedad de la página de propiedades.
-   Cualquier fragmento de código (cliente u objeto) que desee que muestre la hoja de propiedades de un objeto pasa el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto (o una matriz si varios objetos se van a ver afectados) junto con una matriz de CLSID de página a [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), que crea el cuadro de diálogo con pestañas.
-   El cuadro de diálogo de marco de propiedades crea instancias de una única instancia de cada página de propiedades, mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en cada CLSID. El marco de propiedades obtiene al menos un puntero [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) para cada página. Además, el marco crea un objeto de sitio de página de propiedades en sí mismo para cada página. Cada sitio implementa [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) y este puntero se pasa a cada página. A continuación, la página se comunica con el sitio a través de este puntero de interfaz.
-   Cada página también es consciente del objeto u objetos para los que se ha invocado; es decir, el marco de propiedad pasa los punteros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)de los objetos a cada página. Cuando se le indica que aplique los cambios a los objetos, cada página consulta el puntero de interfaz adecuado y pasa los nuevos valores de propiedad a los objetos de la forma que desee. No hay ninguna necesidad de establecer la comunicación.
-   Un objeto también puede admitir la exploración por propiedad mediante la interfaz [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) , lo que permite al objeto especificar qué propiedad debe recibir el foco inicial cuando se muestra la página de propiedades y especificar cadenas y valores que el cliente puede mostrar en su propia interfaz de usuario.

Estas características se muestran en el diagrama siguiente:

![Diagrama que muestra las características hojas de propiedades y páginas de propiedades.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Estas interfaces se definen de la siguiente manera:

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

El método [**ISpecifyPropertyPages:: GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) devuelve una matriz contada de valores UUID (GUID) cada uno de los cuales describe el CLSID de una página de propiedades que el objeto desea mostrar. Quien llama a la hoja de propiedades con [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) pasa esta matriz a la función. Tenga en cuenta que si el autor de la llamada desea mostrar páginas de propiedades de varios objetos, solo debe pasar la intersección de las listas de CLSID de todos los objetos a estas funciones. En otras palabras, el autor de la llamada solo debe invocar las páginas de propiedades que son comunes a todos los objetos.

Además, el llamador pasa también los punteros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) a los objetos afectados a las funciones de la API. Ambas funciones de la API crean un cuadro de diálogo de marco de propiedades y crean una instancia de un sitio de página con [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) para cada página que se va a cargar. A través de esta interfaz, una página de propiedades puede:

-   Recupere el idioma actual usado en la hoja de propiedades a través de [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Pida al marco que procese las pulsaciones de teclas a través de [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Notifique al fotograma los cambios en la página a través de [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Obtiene un puntero de interfaz para el propio marco a través de [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), aunque en este momento no hay interfaces definidas para el marco para esta función devuelve E \_ NOTIMPL.

El marco de propiedades crea instancias de cada objeto de página de propiedades y obtiene la interfaz [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) de cada página. A través de esta interfaz, el marco informa a la página de su sitio de página ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), recupera las dimensiones y cadenas de la página ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), pasa los punteros de interfaz a los objetos afectados ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), indica a la página cuándo crear y destruir sus controles ([**Activar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) [**y desactivar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)). indica a la página que se muestre o se cambie de posición ([**Mostrar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) y [**mover**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), indica a la página que aplique sus valores actuales a los objetos afectados ([**Apply**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), comprueba el estado de modificación de la página ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), invoca la ayuda ([**ayuda**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) y pasa las pulsaciones de tecla a la página ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Un objeto también puede admitir la exploración por propiedad, que proporciona:

1.  Una forma (a través de [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) y [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) para especificar qué propiedad de la página de propiedades debe recibir el foco inicial cuando se muestra por primera vez una hoja de propiedades.
2.  Una manera (a través de [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) para que el objeto especifique valores predefinidos y sus correspondientes cadenas descriptivas que podrían mostrarse en la propia interfaz de usuario de un cliente para las propiedades.

Un objeto puede elegir admitir (2) sin admitir (1), como cuando el objeto no tiene ninguna hoja de propiedades.

Las interfaces [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) y [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) se definen de la siguiente manera:

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Para especificar su compatibilidad con estas funcionalidades, el objeto implementa [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). A través de esta interfaz, el llamador puede solicitar la información necesaria para lograr la exploración, como cadenas predefinidas ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) y valores ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), así como una cadena de presentación para una propiedad determinada ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Además, el cliente puede obtener el CLSID de la página de propiedades que permite al usuario editar una propiedad determinada identificada con un DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). A continuación, el cliente indica al marco de propiedades que Active esa página inicialmente pasando el CLSID y el DISPID a [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). El marco activa primero esa página y pasa el DISPID a la página a través de [**IPropertyPage2:: EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). A continuación, la página establece el foco en el campo de edición de esa propiedad. De esta manera, un cliente puede pasar de un nombre de propiedad en su propia interfaz de usuario a la página de propiedades que puede manipular esa propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




