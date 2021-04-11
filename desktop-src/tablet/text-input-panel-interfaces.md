---
description: Esta sección contiene información acerca de las interfaces que se usan para controlar la apariencia y el comportamiento del panel de entrada de Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfaces del panel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279158"
---
# <a name="text-input-panel-interfaces"></a>Interfaces del panel de entrada de texto

Esta sección contiene información acerca de las interfaces que se usan para controlar la apariencia y el comportamiento del panel de entrada de Tablet PC.

> [!Note]  
> Las interfaces del panel de entrada de texto no son compatibles con la automatización.

 

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Lo utiliza el código de entrada de texto personalizado de la aplicación para insertar el texto en el campo de texto y en el almacén de respaldo de servicios de texto.<br/> |
| [**Interfaz ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Proporciona control sobre el panel de entrada de Tablet PC.<br/>                                                                                  |
| [**Interfaz ITextInputPanelEventSink**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Define métodos que controlan los eventos de la [**interfaz ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .<br/>                                      |
| [**Interfaz ITextInputPanelRunInfo**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Proporciona un método para determinar si el panel de entrada de texto se está ejecutando actualmente.<br/>                                                      |
| [**Interfaz ITipAutocompleteClient**](itipautocompleteclient.md)       | Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.<br/>                                      |
| [**Interfaz ITipAutocompleteProvider**](itipautocompleteprovider.md)   | Administra el lado de la aplicación de la integración de autocompletar del panel de entrada de texto.<br/>                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




