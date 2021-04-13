---
title: Accesibilidad de controles ActiveX sin ventanas
description: En esta sección se describe cómo usar la API de accesibilidad de Windows para asegurarse de que se pueda tener acceso a los controles ActiveX sin ventanas de Microsoft.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421103"
---
# <a name="windowless-activex-control-accessibility"></a>Accesibilidad de controles ActiveX sin ventanas

En esta sección se describe cómo usar la API de accesibilidad de Windows para asegurarse de que se pueda tener acceso a los controles ActiveX sin ventanas de Microsoft.

Windows 8 incluye nuevas interfaces de API de accesibilidad de Windows que simplifican la tarea de implementar la accesibilidad para controles ActiveX sin ventanas. La API incluye interfaces que se implementan en un control sin ventanas y en el contenedor de controles, lo que permite que el control sin ventanas y su contenedor funcionen juntos para proporcionar información de accesibilidad sobre el control sin ventanas. La API admite los siguientes escenarios:

-   Microsoft Active Accessibility controles sin ventanas hospedados en un contenedor de control de Microsoft Active Accessibility.
-   Microsoft Active Accessibility controles sin ventanas hospedados en un contenedor de controles de automatización de la interfaz de usuario de Microsoft.
-   Controles sin ventana de automatización de la interfaz de usuario hospedados en un contenedor de control de Microsoft Active Accessibility.
-   Controles sin ventana de automatización de la interfaz de usuario hospedados en un contenedor de control de UI Automation.

En la tabla siguiente se enumeran las interfaces que admiten los controles ActiveX sin ventanas y se identifican los objetos que implementan las interfaces.



| Object              | MSAA                                                                             | automatización de la interfaz de usuario                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objeto de control      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Sitio de control        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Raíz de la ventana host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>En esta sección

-   [Cómo usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Cómo usar MSAA para hacer que un control ActiveX sin ventanas sea accesible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Cómo hospedar un control ActiveX sin ventanas de automatización de la interfaz de usuario](host-a-ui-automation-windowless-activex-control.md)
-   [Cómo hospedar un control ActiveX sin ventanas de MSAA](host-an-msaa-windowless-activex-control.md)

 

 