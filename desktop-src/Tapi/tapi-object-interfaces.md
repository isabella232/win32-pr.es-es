---
description: El objeto TAPI es el objeto principal de TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces de objeto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678233"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="f878d-103">Interfaces de objeto TAPI</span><span class="sxs-lookup"><span data-stu-id="f878d-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="f878d-104">El [objeto TAPI](tapi-object.md) es el objeto principal de TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="f878d-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="f878d-105">La interfaz [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) no se expone directamente en el objeto TAPI, pero está estrechamente relacionada con ella y se muestra aquí para mayor comodidad de referencia.</span><span class="sxs-lookup"><span data-stu-id="f878d-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="f878d-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f878d-106">Interfaces</span></span>                                                 | <span data-ttu-id="f878d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f878d-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f878d-108">**ITTAPI**</span><span class="sxs-lookup"><span data-stu-id="f878d-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="f878d-109">Interfaz TAPI 3 principal.</span><span class="sxs-lookup"><span data-stu-id="f878d-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="f878d-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="f878d-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="f878d-111">Deriva de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); proporciona métodos adicionales que admiten dispositivos telefónicos.</span><span class="sxs-lookup"><span data-stu-id="f878d-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="f878d-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="f878d-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="f878d-113">Interfaz de salida que se usa para recibir información asincrónica acerca de los eventos TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="f878d-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="f878d-114">**ITTAPICallCenter**</span><span class="sxs-lookup"><span data-stu-id="f878d-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="f878d-115">Proporciona una interfaz de entrada en los controles del centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f878d-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="f878d-116">**ITTAPIObjectEvent**</span><span class="sxs-lookup"><span data-stu-id="f878d-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="f878d-117">Proporciona métodos para recuperar información relacionada con eventos de objetos TAPI.</span><span class="sxs-lookup"><span data-stu-id="f878d-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="f878d-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="f878d-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="f878d-119">Extiende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); proporciona un método para recuperar un puntero al objeto de teléfono que causó el evento de objeto TAPI.</span><span class="sxs-lookup"><span data-stu-id="f878d-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
