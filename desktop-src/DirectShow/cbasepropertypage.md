---
description: La clase CBasePropertyPage es una clase abstracta para implementar una página de propiedades. Utilice esta clase si está escribiendo un filtro (u otro objeto) que admita páginas de propiedades.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Clase CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671256"
---
# <a name="cbasepropertypage-class"></a>Clase CBasePropertyPage

![jerarquía de clases cbasepropertypage](images/cprop01.png)

La `CBasePropertyPage` clase es una clase abstracta para implementar una página de propiedades. Utilice esta clase si está escribiendo un filtro (u otro objeto) que admita páginas de propiedades.



| Variables de miembro protegidas                                             | Descripción                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bDirty**](cbasepropertypage-m-bdirty.md)                        | Indica si alguna de las propiedades ha cambiado.                                                                             |
| [**m \_ DialogId**](cbasepropertypage-m-dialogid.md)                    | Identificador de recurso del cuadro de diálogo.                                                                                               |
| [**m \_ Dlg**](cbasepropertypage-m-dlg.md)                              | Identificador de la ventana de cuadro de diálogo.                                                                                                      |
| [**m \_ hWnd**](cbasepropertypage-m-hwnd.md)                            | Identificador de la ventana de cuadro de diálogo.                                                                                                      |
| [**m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)                  | Puntero a la interfaz **IPropertyPageSite** del sitio de la página de propiedades.                                                         |
| [**c \_ idcargo**](cbasepropertypage-m-titleid.md)                      | Identificador de recurso de una cadena que contiene el título del cuadro de diálogo.                                                                  |
| Métodos públicos                                                         | Descripción                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | Método de constructor.                                                                                                               |
| [**~ CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | Método de destructor. Virtualiza.                                                                                                       |
| [**OnActivate**](cbasepropertypage-onactivate.md)                     | Se le llama cuando se activa la página de propiedades. Virtualiza.                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | Se llama cuando el usuario aplica los cambios a la página de propiedades. Virtualiza.                                                               |
| [**Conectar**](cbasepropertypage-onconnect.md)                       | Proporciona un puntero **IUnknown** al objeto asociado a la página de propiedades. Virtualiza.                                        |
| [**Desactivar**](cbasepropertypage-ondeactivate.md)                 | Se llama cuando se destruye la ventana del cuadro de diálogo. Virtualiza.                                                                          |
| [**Desconectar**](cbasepropertypage-ondisconnect.md)                 | Se llama cuando la página de propiedades debe liberar el objeto asociado. Virtualiza.                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | Se llama cuando el cuadro de diálogo recibe un mensaje. Virtualiza.                                                                           |
| Métodos IPropertyPage                                                  | Descripción                                                                                                                       |
| [**Activar**](cbasepropertypage-activate.md)                         | Crea la ventana de cuadro de diálogo.                                                                                                    |
| [**Aplicar**](cbasepropertypage-apply.md)                               | Aplica los valores de la página de propiedades actual al objeto asociado a la página de propiedades.                                          |
| [**Desactivación**](cbasepropertypage-deactivate.md)                     | Destruye la ventana de cuadro de diálogo.                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | Recupera información sobre la página de propiedades.                                                                                    |
| [**Ayuda**](cbasepropertypage-help.md)                                 | Invoca la ayuda de la página de propiedades.                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | Indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a **IPropertyPage:: Apply**. |
| [**Move**](cbasepropertypage-move.md)                                 | Coloca y cambia el tamaño del cuadro de diálogo.                                                                                             |
| [**SetObjects**](cbasepropertypage-setobjects.md)                     | Proporciona punteros **IUnknown** para los objetos asociados a la página de propiedades.                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | Inicializa la página de propiedades.                                                                                                    |
| [**Feria**](cbasepropertypage-show.md)                                 | Muestra u oculta el cuadro de diálogo.                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | Indica a la página de propiedades que procese una pulsación de tecla.                                                                               |



 

## <a name="remarks"></a>Observaciones

Una página de propiedades es un objeto COM, por lo que debe generar un GUID para el identificador de clase (CLSID) y proporcionar una entrada en la matriz [**CFactoryTemplate**](cfactorytemplate.md) . Para obtener más información, vea [DirectShow y com](directshow-and-com.md). En el ejemplo siguiente se muestra una entrada de generador de clases típica:


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



El filtro debe exponer la interfaz **ISpecifyPropertyPages** . Esta interfaz contiene un método único, **GetPages**, que devuelve el CLSID de la página de propiedades. En el ejemplo siguiente se muestra cómo implementar este método:


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



No olvide reemplazar también el método **NonDelegatingQueryInterface** del filtro. Para obtener más información, vea [DirectShow y com](directshow-and-com.md) y [**INonDelegatingUnknown**](inondelegatingunknown.md).

A continuación, cree el cuadro de diálogo como un recurso en el proyecto y cree un recurso de cadena que contenga el título del cuadro de diálogo. Ambos identificadores de recursos son parámetros para el constructor **CBasePropertyPage** . Mantener la cadena de título en un recurso facilita la localización de la página de propiedades.

La clase **CBasePropertyPage** proporciona un marco para la interfaz **IPropertyPage** . Este marco de trabajo llama a una serie de métodos virtuales, entre los que se incluyen [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md), etc. En la clase base, estos métodos simplemente devuelven los valores \_ correctos. La clase derivada deberá invalidar algunos o todos estos métodos virtuales. Para obtener más información, vea los comentarios de los métodos individuales.

Para obtener un ejemplo de cómo usar esta clase para crear una página de propiedades, vea [crear una página de propiedades de filtro](creating-a-filter-property-page.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




