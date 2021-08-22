---
title: Accesibilidad del control ActiveX sin ventanas
description: En esta sección se describe cómo usar el Windows API de accesibilidad para asegurarse de que los controles de ActiveX de Microsoft sin ventanas son accesibles.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563460"
---
# <a name="windowless-activex-control-accessibility"></a>Accesibilidad del control ActiveX sin ventanas

En esta sección se describe cómo usar el Windows API de accesibilidad para asegurarse de que los controles de ActiveX de Microsoft sin ventanas son accesibles.

Windows 8 nuevas interfaces Windows API de accesibilidad que simplifican la tarea de implementar la accesibilidad para controles de ActiveX sin ventanas. La API incluye interfaces que se implementan en un control sin ventanas y en el contenedor de controles, lo que permite que el control sin ventanas y su contenedor funcionen conjuntamente para proporcionar información de accesibilidad sobre el control sin ventana. La API admite los siguientes escenarios:

-   Microsoft Active Accessibility controles sin ventanas hospedados en un contenedor Microsoft Active Accessibility control.
-   Microsoft Active Accessibility controles sin ventana hospedados en un contenedor de controles Automatización de la interfaz de usuario Microsoft.
-   Automatización de la interfaz de usuario controles sin ventanas hospedados en un contenedor Microsoft Active Accessibility control.
-   Automatización de la interfaz de usuario controles sin ventanas hospedados en un contenedor Automatización de la interfaz de usuario control.

En la tabla siguiente se enumeran las interfaces que admiten controles de ActiveX sin ventanas e identifica los objetos que implementan las interfaces.



| Object              | MSAA                                                                             | automatización de la interfaz de usuario                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objeto de control      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Sitio de control        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Raíz de la ventana host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>En esta sección

-   [Cómo usar Automatización de la interfaz de usuario para que un control de ActiveX sin ventanas sea accesible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Cómo usar MSAA para hacer que un control de ActiveX sin ventanas sea accesible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Cómo hospedar un control Automatización de la interfaz de usuario sin ActiveX ventana](host-a-ui-automation-windowless-activex-control.md)
-   [Cómo hospedar un control de ActiveX sin ventanas de MSAA](host-an-msaa-windowless-activex-control.md)

 

 