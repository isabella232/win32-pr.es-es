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
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="500e3-103">Interfaces del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="500e3-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="500e3-104">Esta sección contiene información acerca de las interfaces que se usan para controlar la apariencia y el comportamiento del panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="500e3-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="500e3-105">Las interfaces del panel de entrada de texto no son compatibles con la automatización.</span><span class="sxs-lookup"><span data-stu-id="500e3-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="500e3-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="500e3-106">In This Section</span></span>



| <span data-ttu-id="500e3-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="500e3-107">Interface</span></span>                                                                | <span data-ttu-id="500e3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="500e3-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="500e3-109">**Interfaz IHandWrittenTextInsertion**</span><span class="sxs-lookup"><span data-stu-id="500e3-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="500e3-110">Lo utiliza el código de entrada de texto personalizado de la aplicación para insertar el texto en el campo de texto y en el almacén de respaldo de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="500e3-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="500e3-111">**Interfaz ITextInputPanel**</span><span class="sxs-lookup"><span data-stu-id="500e3-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="500e3-112">Proporciona control sobre el panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="500e3-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="500e3-113">**Interfaz ITextInputPanelEventSink**</span><span class="sxs-lookup"><span data-stu-id="500e3-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="500e3-114">Define métodos que controlan los eventos de la [**interfaz ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .</span><span class="sxs-lookup"><span data-stu-id="500e3-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="500e3-115">**Interfaz ITextInputPanelRunInfo**</span><span class="sxs-lookup"><span data-stu-id="500e3-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="500e3-116">Proporciona un método para determinar si el panel de entrada de texto se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="500e3-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="500e3-117">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="500e3-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="500e3-118">Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="500e3-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="500e3-119">**Interfaz ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="500e3-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="500e3-120">Administra el lado de la aplicación de la integración de autocompletar del panel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="500e3-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="500e3-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="500e3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="500e3-122">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="500e3-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




