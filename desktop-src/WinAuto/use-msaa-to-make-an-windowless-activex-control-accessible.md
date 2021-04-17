---
title: Usar MSAA para hacer que un control ActiveX sin ventanas sea accesible
description: Describe cómo usar Microsoft Active Accessibility \ 32; API para asegurarse de que el control Microsoft ActiveX sin ventanas está accesible para las aplicaciones cliente de tecnología de asistencia (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Control ActiveX, accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704997"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Usar MSAA para hacer que un control ActiveX sin ventanas sea accesible

Describe cómo usar la API de Microsoft Active Accessibility para asegurarse de que el control ActiveX sin ventanas de Microsoft es accesible para las aplicaciones cliente de tecnología de asistencia (AT).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de Microsoft Win32 y del modelo de objetos componentes (COM)
-   Controles ActiveX sin ventanas
-   Servidores de Microsoft Active Accessibility

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implement-the-iaccessible-interface"></a>Paso 1: implementar la interfaz IAccessible.

Para que el control ActiveX sin ventanas sea accesible, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de Microsoft Active Accessibility, del mismo modo que lo haría para un control basado en ventanas, excepto como se describe en los pasos siguientes. Para obtener más información sobre cómo implementar **IAccessible**, consulte [la guía del desarrollador para Active Accessibility servidores](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Paso 2: implementar la interfaz IServiceProvider.

Cuando un cliente solicita información de accesibilidad sobre el control sin ventana, el contenedor llama al método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del control para recuperar el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

En este ejemplo se muestra cómo implementar el método [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Paso 3: delegue las llamadas al método IAccessible:: get \_ accParent en el método IAccessibleWindowlessSite:: GetParentAccessible del sitio de control.

Cuando un cliente solicita el objeto primario del control sin ventana, el contenedor llama al método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del control. La implementación **Get \_ accParent** debe delegar al método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenedor.

Este ejemplo muestra cómo implementar el método [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Paso 4: adquirir un intervalo de identificadores de objeto para asignar a los orígenes de eventos en el control sin ventana.

Al igual que los controles basados en ventanas, un control ActiveX sin ventanas llama a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar a los clientes de eventos importantes. Los parámetros de función incluyen el ID. de objeto del elemento que está generando el evento. El control sin ventana debe asignar identificadores de objeto mediante un valor de un intervalo adquirido llamando al método [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sitio de control.

En este ejemplo se muestra cómo adquirir un intervalo de valores de ID. de objeto del contenedor de control.


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Paso 5: implementar la interfaz IAccessibleHandler.

Cuando un control sin ventana llama a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , el control especifica el identificador de objeto del elemento de la interfaz de usuario que está generando el evento y especifica el contenedor de control como la ventana que responderá a los mensajes de [**WM \_ GETOBJECT**](wm-getobject.md) en nombre del control.

Si una aplicación cliente responde al evento, el contenedor de control recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) que incluye el identificador de objeto del elemento de la interfaz de usuario que ha generado el evento. El contenedor de control responde buscando el control sin ventanas que "posee" el identificador de objeto y, a continuación, llamando al método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ese control. El método **AccessibleObjectFromID** devuelve el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y el contenedor de control reenvía el puntero a la aplicación cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accesibilidad de controles ActiveX sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 