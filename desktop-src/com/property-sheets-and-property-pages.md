---
title: Hojas de propiedades y páginas de propiedades
description: Hojas de propiedades y páginas de propiedades
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104943"
---
# <a name="property-sheets-and-property-pages"></a>Hojas de propiedades y páginas de propiedades

Las propiedades de un objeto se exponen a los clientes igual que los métodos a través de interfaces COM o la implementación **de IDispatch** del objeto, lo que permite que los programas que llaman a estos métodos cambien las propiedades. La tecnología OLE de las páginas de propiedades proporciona los medios para compilar una interfaz de usuario para las propiedades de un objeto de acuerdo con Windows de interfaz de usuario. Por lo tanto, las propiedades se exponen a los usuarios finales. La hoja de propiedades de un objeto es un diálogo con pestañas donde cada pestaña corresponde a una página de propiedades específica. El modelo OLE para trabajar con páginas de propiedades consta de estas características:

-   Cada página de propiedades se administra mediante un objeto en proceso que implementa [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) o [**IPropertyPage2.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) Cada página se identifica con su propio CLSID único.
-   Un objeto especifica su compatibilidad con las páginas de propiedades mediante la implementación [**de ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). A través de esta interfaz, el autor de la llamada puede obtener una lista de CLID que identifican las páginas de propiedades específicas que admite el objeto. Si el objeto especifica un CLSID de página de propiedades, el objeto debe ser capaz de recibir cambios de propiedad de la página de propiedades.
-   Cualquier fragmento de código (cliente u objeto) que quiera mostrar la hoja de propiedades de un objeto pasa el puntero [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto (o una matriz si se van a ver afectados varios objetos) junto con una matriz de CLID de página a [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), que crea el cuadro de diálogo con pestañas.
-   El cuadro de diálogo de marco de propiedades crea una instancia única de cada página de propiedades mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en cada CLSID. El marco de propiedades obtiene al menos un [**puntero IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) para cada página. Además, el marco crea un objeto de sitio de página de propiedades en sí mismo para cada página. Cada sitio implementa [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) y este puntero se pasa a cada página. A continuación, la página se comunica con el sitio a través de este puntero de interfaz.
-   Cada página también es consciente del objeto u objetos para los que se ha invocado. es decir, el marco de propiedades pasa los punteros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)de los objetos a cada página. Cuando se le indica que aplique cambios a los objetos, cada página consulta el puntero de interfaz adecuado y pasa nuevos valores de propiedad a los objetos de la manera deseada. No hay ninguna información sobre cómo debe producirse dicha comunicación.
-   Un objeto también puede admitir la exploración por propiedad a través de la interfaz [**IPerPropertyBrowsing,**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) lo que permite al objeto especificar qué propiedad debe recibir el foco inicial cuando se muestra la página de propiedades y especificar cadenas y valores que el cliente puede mostrar en su propia interfaz de usuario.

Estas características se ilustran en el diagrama siguiente:

![Diagrama que muestra las hojas de propiedades y las características de las páginas de propiedades.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

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

El [**método ISpecifyPropertyPages::GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) devuelve una matriz con recuento de valores UUID (GUID) que describen el CLSID de una página de propiedades que el objeto desea mostrar. El que invoca la hoja de propiedades [**con OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) pasa esta matriz a la función. Tenga en cuenta que si el autor de la llamada desea mostrar páginas de propiedades para varios objetos, solo debe pasar la intersección de las listas CLSID de todos los objetos a estas funciones. En otras palabras, el autor de la llamada solo debe invocar páginas de propiedades que sean comunes a todos los objetos.

Además, el autor de la llamada pasa también los punteros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) a los objetos afectados a las funciones de API. Ambas funciones de API crean un cuadro de diálogo de marco de propiedades y crean una instancia de un sitio de página [**con IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) para cada página que cargará. A través de esta interfaz, una página de propiedades puede:

-   Recupere el idioma actual usado en la hoja de propiedades a través [**de GetLocaleID.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid)
-   Pida al marco que procese las pulsaciones de tecla [**a través de TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Notifique al marco de cambios en la página a través [**de OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Obtenga un puntero de interfaz para el propio marco a través de [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), aunque no haya ninguna interfaz definida para el marco en este momento para esta función siempre devuelve E \_ NOTIMPL.

El marco de propiedades crea instancias de cada objeto de página de propiedades y obtiene la [**interfaz IPropertyPage de cada**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) página. A través de esta interfaz, el marco informa a la página de su sitio de página [**(SetPageSite),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)recupera las dimensiones de página y las cadenas [**(GetPageInfo),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)pasa los punteros de interfaz a los objetos afectados [**(SetObjects),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)indica a la página cuándo crear y destruir sus controles [**(Activar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) y [**Desactivar),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)indica a la página para mostrar o cambiar la posición [**(Mostrar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) y [**mover),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)indica a la página que aplique sus valores actuales a los objetos afectados [**(Aplicar),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)comprueba el estado desfasado de la página ([**IsPageDirty),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)invoca ayuda [**(Ayuda)**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)y pasa pulsaciones de tecla a la página ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Un objeto también puede admitir la exploración por propiedad, que proporciona:

1.  Una manera (a través de [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) e [**IPropertyPage2)**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)de especificar qué propiedad en qué página de propiedades se debe proporcionar el foco inicial cuando se muestra por primera vez una hoja de propiedades
2.  Una manera (a través de [**IPerPropertyBrowsing)**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)para que el objeto especifique valores predefinidos y las cadenas descriptivas correspondientes que podrían mostrarse en la propia interfaz de usuario de un cliente para las propiedades.

Un objeto puede optar por admitir (2) sin admitir (1), como cuando el objeto no tiene ninguna hoja de propiedades.

Las [**interfaces IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) [**e IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) se definen de la siguiente manera:

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

Para especificar su compatibilidad con estas funcionalidades, el objeto implementa [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). A través de esta interfaz, el autor de la llamada puede solicitar la información necesaria para lograr la exploración, como cadenas predefinidas [**(GetPredefinedStrings)**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)y valores ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), así como una cadena de presentación para una propiedad determinada [**(GetDisplayString).**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)

Además, el cliente puede obtener el CLSID de la página de propiedades que permite al usuario editar una propiedad determinada identificada con un DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). A continuación, el cliente indica al marco de propiedades que active esa página inicialmente pasando clsid y dispid a [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). El marco activa esa página primero y pasa dispid a la página a través [**de IPropertyPage2::EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). A continuación, la página establece el foco en el campo de edición de esa propiedad. De este modo, un cliente puede saltar de un nombre de propiedad en su propia interfaz de usuario a la página de propiedades que puede manipular esa propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




