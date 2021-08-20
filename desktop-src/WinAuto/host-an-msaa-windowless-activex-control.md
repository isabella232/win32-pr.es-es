---
title: Cómo hospedar un control de ActiveX sin ventanas de MSAA
description: Obtenga información sobre cómo crear un contenedor de controles que pueda hospedar controles de Microsoft ActiveX sin ventanas que implementen Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, control de ActiveX ventana
- Control de ActiveX sin ventanas, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115136"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Cómo hospedar un control de ActiveX sin ventanas de MSAA

Obtenga información sobre cómo crear un contenedor de controles que pueda hospedar controles de Microsoft ActiveX sin ventanas que implementen Microsoft Active Accessibility. Siguiendo los pasos descritos aquí, puede asegurarse de que todos los controles sin ventanas basados en Microsoft Active Accessibility que se hospedan en el contenedor de control sean accesibles para las aplicaciones cliente de tecnología de asistencia (AT).

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

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Paso 1: Proporcione la interfaz IAccessible raíz en nombre del control sin ventana.

Siempre que el sistema necesite el [**puntero IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para la raíz de un control sin ventana, el sistema consulta el contenedor de controles. Para recuperar el puntero, el contenedor llama a la implementación del control sin ventanas del [**método IServiceProvider::QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))

Si el contenedor de controles tiene Microsoft Active Accessibility implementación, puede devolver el puntero [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del control sin ventana al sistema.

Si el contenedor de controles tiene una implementación de Microsoft Automatización de la interfaz de usuario, llame a la función [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) para obtener un puntero de interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que represente el control y, a continuación, devuelva el puntero de interfaz **IRawElementProviderSimple** al sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Paso 2: Responder al mensaje \_ WM GETOBJECT en nombre del control sin ventanas.

Cuando una aplicación cliente responde a un winEvent que genera un control sin ventana, el contenedor de controles recibe un mensaje [**\_ WM GETOBJECT**](wm-getobject.md) en nombre del control. El mensaje incluye el identificador de objeto del control sin ventanas que ha producido el evento.

El contenedor de controles responde buscando el control sin ventanas que "posee" el identificador de objeto y, a continuación, llamando al método [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ese control. El **método AccessibleObjectFromID** devuelve el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y el contenedor de controles devuelve el puntero al sistema, que lo reenvía a la aplicación cliente.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Paso 3: Implementar la interfaz IAccessibleWindowlessSite.

1.  Implemente [**el método IAccessibleWindowlessSite::GetParentAccessible.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible)

    Cuando una aplicación cliente necesita información de accesibilidad sobre el elemento primario del proveedor raíz del control sin ventanas, el sistema llama al método [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del control sin ventanas. El control responde llamando al método [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenedor de controles, que proporciona el puntero [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento primario del control sin ventana.

2.  Implemente [**los métodos IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)y [**ReleaseObjectIdRange.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange)

    El contenedor de controles debe mantener una asignación de intervalos de identificadores de objeto a controles sin ventana. La asignación permite al contenedor de controles identificar el control que debe responder a una solicitud determinada de un identificador de objeto. En la tabla siguiente se muestra un ejemplo de asignación de intervalos de identificador de objeto a controles sin ventana.

    

    | Base de intervalo | Tamaño del intervalo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Control 1 |
    | 1.500       | 1000       | Control 2 |
    | 2.500       | 2000       | Control 1 |

    

     

    El contenedor de controles debe mantener la asignación de intervalos de identificador de objeto a controles sin ventana para sí mismo y para todos los elementos secundarios sin ventana. No es necesario que los intervalos de identificadores de objeto sean adyacentes entre sí. Además, para evitar ataques por denegación de servicio, el contenedor de control puede establecer límites en el número de intervalos que se conceden a un control determinado. Sin embargo, es útil permitir más de un intervalo por control para permitir que un control crezca.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Paso 4: Opcional: Implemente la interfaz IAccessibleHostingElementProviders.

Implemente la [**interfaz IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) si el contenedor de controles tiene una implementación de servidor Microsoft Active Accessibility y el servidor es la raíz de un árbol de accesibilidad que incluye controles ActiveX sin ventanas que admiten Automatización de la interfaz de usuario. La interfaz **IAccessibleHostingElementProviders** tiene un único método, [**GetEmbeddedFragmentRoots,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)que recupera los puntero Automatización de la interfaz de usuario s de interfaz [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) de todos los controles ActiveX sin ventana que hospeda el contenedor de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo hospedar un control Automatización de la interfaz de usuario sin ActiveX ventana](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Accesibilidad del control ActiveX sin ventanas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 