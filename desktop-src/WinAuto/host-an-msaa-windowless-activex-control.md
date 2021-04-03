---
title: Cómo hospedar un control ActiveX sin ventanas de MSAA
description: Aprenda a crear un contenedor de controles que puede hospedar controles ActiveX de Microsoft en ventanas que implementan Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- Control ActiveX de MSAA y sin ventanas
- Control ActiveX sin ventanas, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791793"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Cómo hospedar un control ActiveX sin ventanas de MSAA

Aprenda a crear un contenedor de controles que puede hospedar controles ActiveX de Microsoft en ventanas que implementan Microsoft Active Accessibility. Siguiendo los pasos que se describen aquí, puede asegurarse de que los controles sin ventanas basados en Microsoft Active Accessibility que se hospedan en el contenedor de control son accesibles a las aplicaciones cliente de tecnología de asistencia (AT).

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

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Paso 1: proporcionar la interfaz IAccessible raíz en nombre del control sin ventana.

Siempre que el sistema necesita el puntero [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para la raíz de un control sin ventana, el sistema consulta el contenedor del control. Para recuperar el puntero, el contenedor llama a la implementación del control sin ventana del método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Si el contenedor de control tiene una implementación de Microsoft Active Accessibility, puede devolver el puntero [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del control sin ventana al sistema.

Si el contenedor de control tiene una implementación de automatización de la interfaz de usuario de Microsoft, llame a la función [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) para obtener un puntero de interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que represente el control y, a continuación, devuelva el puntero de interfaz **IRawElementProviderSimple** al sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Paso 2: responder al \_ mensaje de WM GETOBJECT en nombre del control sin ventana.

Cuando una aplicación cliente responde a un WinEvent generado por un control sin ventana, el contenedor de control recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) en nombre del control. El mensaje incluye el identificador de objeto del control sin ventana que ha generado el evento.

El contenedor de control responde buscando el control sin ventanas que "posee" el identificador de objeto y, a continuación, llamando al método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ese control. El método **AccessibleObjectFromID** devuelve el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y el contenedor de control devuelve el puntero al sistema, que lo reenvía a la aplicación cliente.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Paso 3: implementar la interfaz IAccessibleWindowlessSite.

1.  Implemente el método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) .

    Cuando una aplicación cliente necesita información de accesibilidad sobre el elemento primario del proveedor raíz del control sin ventana, el sistema llama al método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del control sin ventana. El control responde llamando al método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenedor de control, que proporciona el puntero [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento primario del control sin ventana.

2.  Implemente los métodos [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)y [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    El contenedor de control debe mantener una asignación de intervalos de ID. de objeto a controles sin ventanas. La asignación permite al contenedor de control identificar el control que debe responder a una solicitud determinada para un identificador de objeto. En la tabla siguiente se muestra un ejemplo de asignación de intervalos de ID. de objeto a controles sin ventanas.

    

    | Base de intervalo | Tamaño de intervalo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Control 1 |
    | 1.500       | 1000       | Control 2 |
    | 2.500       | 2000       | Control 1 |

    

     

    El contenedor de controles debe mantener la asignación de los intervalos de ID. de objeto a controles sin ventanas para sí mismo y para todos los elementos secundarios sin ventanas. Los intervalos de ID. de objeto no tienen por qué ser adyacentes entre sí. Además, para evitar ataques por denegación de servicio, el contenedor de control puede establecer límites en el número de intervalos que se conceden a un control determinado. Sin embargo, resulta útil permitir más de un intervalo por control, para permitir que un control crezca.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Paso 4: opcional: implemente la interfaz IAccessibleHostingElementProviders.

Implemente la interfaz [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) si el contenedor de control tiene una implementación de servidor de Microsoft Active Accessibility y el servidor es la raíz de un árbol de accesibilidad que incluye controles ActiveX sin ventanas que admiten la automatización de la interfaz de usuario. La interfaz **IAccessibleHostingElementProviders** tiene un único método, [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), que recupera los punteros de interfaz [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) de todos los controles ActiveX sin ventanas de automatización de la interfaz de usuario que se hospedan en el contenedor de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo hospedar un control ActiveX sin ventanas de automatización de la interfaz de usuario](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Accesibilidad de controles ActiveX sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 