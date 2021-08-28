---
title: Uso de MSAA para hacer que un control de ActiveX sin ventanas sea accesible
description: Describe cómo usar el Microsoft Active Accessibility \ 32; API para asegurarse de que las aplicaciones cliente de tecnología de asistencia (AT) pueden acceder al control de ActiveX sin ventanas de Microsoft.
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX Control, accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bac5c4d2a27e5f069f2242999438eebe85e2ea7df1a6bc94890aec142db246c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098115"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Uso de MSAA para hacer que un control de ActiveX sin ventanas sea accesible

Describe cómo usar la API Microsoft Active Accessibility para asegurarse de que el control ActiveX de Microsoft sin ventanas es accesible para las aplicaciones cliente de tecnología de asistencia (AT).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Programación de Microsoft Win32 y Component Object Model (COM)
-   Controles de ActiveX sin ventanas
-   Microsoft Active Accessibility servidores

## <a name="instructions"></a>Instructions

### <a name="step-1-implement-the-iaccessible-interface"></a>Paso 1: Implementar la interfaz IAccessible.

Para que el control de ActiveX sin ventanas sea accesible, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de Microsoft Active Accessibility, tal como lo haría para un control basado en ventanas, excepto como se describe en los pasos siguientes. Para obtener más información sobre cómo implementar **IAccessible,** vea [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Paso 2: Implementar la interfaz IServiceProvider.

Cuando un cliente solicita información de accesibilidad sobre el control sin ventanas, el contenedor llama al método [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del control para recuperar el puntero de interfaz [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

En este ejemplo se muestra cómo implementar el [**método QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))


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



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Paso 3: Delegar llamadas del método IAccessible::get accParent al método \_ IAccessibleWindowlessSite::GetParentAccessible del sitio de control.

Cuando un cliente solicita el objeto primario del control sin ventana, el contenedor llama al método [**IAccessible::get \_ accParent del**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) control. La **implementación de get \_ accParent** debe delegar al [**método IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenedor.

En este ejemplo se muestra cómo implementar el [**\_ método get accParent.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)


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



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Paso 4: Adquirir un intervalo de los iDs de objeto que se van a asignar a los orígenes de eventos en el control sin ventana.

Al igual que los controles basados en ventanas, un control de ActiveX sin ventana llama a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar a los clientes de eventos importantes. Los parámetros de función incluyen el identificador de objeto del elemento que genera el evento. El control sin ventanas debe asignar los id. de objeto mediante un valor de un intervalo adquirido mediante una llamada al método [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sitio de control.

En este ejemplo se muestra cómo adquirir un intervalo de valores de identificador de objeto desde el contenedor de controles.


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



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Paso 5: Implementar la interfaz IAccessibleHandler.

Cuando un control sin ventana llama a la función [**NotifyWinEvent,**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) el control especifica el identificador de objeto del elemento de interfaz de usuario que genera el evento y especifica el contenedor de controles como la ventana que responderá a los mensajes [**\_ WM GETOBJECT**](wm-getobject.md) en nombre del control.

Si una aplicación cliente responde al evento , el contenedor de controles recibe un mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM que incluye el identificador de objeto del elemento de interfaz de usuario que ha producido el evento. El contenedor de controles responde buscando el control sin ventanas que "posee" el identificador de objeto y, a continuación, llamando al método [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ese control. El **método AccessibleObjectFromID** devuelve el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y el contenedor de controles reenvía el puntero a la aplicación cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Automatización de la interfaz de usuario para que un control de ActiveX sin ventanas sea accesible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accesibilidad del control ActiveX sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 