---
description: ELS admite las funciones definidas en la tabla siguiente.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funciones de servicios lingüísticos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652795"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="8553b-103">Funciones de servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="8553b-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="8553b-104">ELS admite las funciones definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8553b-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="8553b-105">Función</span><span class="sxs-lookup"><span data-stu-id="8553b-105">Function</span></span>                                                 | <span data-ttu-id="8553b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8553b-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8553b-107">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="8553b-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="8553b-108">Función de devolución de llamada definida por la aplicación que procesa asincrónicamente los datos generados por la función **MappingRecognizeText** .</span><span class="sxs-lookup"><span data-stu-id="8553b-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="8553b-109">**MappingDoAction**</span><span class="sxs-lookup"><span data-stu-id="8553b-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="8553b-110">Hace que un servicio ELS realice una acción después de que se haya producido el reconocimiento del texto.</span><span class="sxs-lookup"><span data-stu-id="8553b-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="8553b-111">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="8553b-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="8553b-112">Libera memoria y recursos asignados durante una operación de reconocimiento de texto de ELS.</span><span class="sxs-lookup"><span data-stu-id="8553b-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="8553b-113">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="8553b-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="8553b-114">Libera la memoria y los recursos asignados para que la aplicación interactúe con uno o más servicios de ELS.</span><span class="sxs-lookup"><span data-stu-id="8553b-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="8553b-115">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="8553b-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="8553b-116">Recupera una lista de los servicios compatibles con la plataforma ELS disponibles, junto con la información asociada, según los criterios especificados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8553b-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="8553b-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="8553b-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="8553b-118">Llama a un servicio ELS para reconocer texto.</span><span class="sxs-lookup"><span data-stu-id="8553b-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



