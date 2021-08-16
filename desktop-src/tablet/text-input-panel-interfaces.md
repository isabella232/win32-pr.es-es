---
description: Esta sección contiene información sobre las interfaces que se usan para controlar la apariencia y el comportamiento del panel de entrada de Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfaces del panel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2dcffe1eb67f00b4fe4d2ed3f371af003e040a30213516ae93eab73def6ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715412"
---
# <a name="text-input-panel-interfaces"></a>Interfaces del panel de entrada de texto

Esta sección contiene información sobre las interfaces que se usan para controlar la apariencia y el comportamiento del panel de entrada de Tablet PC.

> [!Note]  
> Las interfaces del Panel de entrada de texto no son compatibles con Automation.

 

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IHandWrittenTextInsertion (Interfaz)**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Lo usa el código de entrada de texto personalizado de la aplicación para insertar el texto tanto en el campo de texto como en el almacén de respaldo de Text Services.<br/> |
| [**ITextInputPanel (interfaz)**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Proporciona control sobre el Panel de entrada de Tablet PC.<br/>                                                                                  |
| [**ITextInputPanelEventSink (Interfaz)**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Define métodos que controlan los eventos de la interfaz [**ITextInputPanel.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)<br/>                                      |
| [**ITextInputPanelRunInfo (Interfaz)**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Proporciona un método para determinar si el Panel de entrada de texto se está ejecutando actualmente.<br/>                                                      |
| [**ITipAutocompleteClient (interfaz)**](itipautocompleteclient.md)       | Permite al cliente llamar al objeto de proveedor autocompletar del Panel de entrada de texto de la aplicación.<br/>                                      |
| [**ITipAutocompleteProvider (interfaz)**](itipautocompleteprovider.md)   | Administra el lado de la aplicación de la integración autocompletar del Panel de entrada de texto.<br/>                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




