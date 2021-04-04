---
description: Al usar el subsistema de tarjeta inteligente, puede comunicarse con tarjetas que podrían no cumplir con las especificaciones ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funciones de acceso directo a tarjetas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907658"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="5e0ed-103">Funciones de acceso directo a tarjetas</span><span class="sxs-lookup"><span data-stu-id="5e0ed-103">Direct Card Access Functions</span></span>

<span data-ttu-id="5e0ed-104">Al usar el subsistema de [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) , puede comunicarse con tarjetas que podrían no cumplir con las especificaciones ISO 7816.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="5e0ed-105">Para ello, las siguientes funciones le permiten controlar los atributos de las comunicaciones entre la aplicación y la tarjeta, ya que le proporcionan una manipulación directa de bajo nivel del [*lector*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="5e0ed-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="5e0ed-106">Para usar estas funciones, debe proporcionar un identificador para el atributo en cuestión.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="5e0ed-107">En el caso de los identificadores y valores de atributo válidos, consulte la tabla 3-1 en *requisitos para los dispositivos de interfaz de PC-Connected*.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="5e0ed-108">Tema</span><span class="sxs-lookup"><span data-stu-id="5e0ed-108">Topic</span></span>                                    | <span data-ttu-id="5e0ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e0ed-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="5e0ed-110">**SCardControl**</span><span class="sxs-lookup"><span data-stu-id="5e0ed-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="5e0ed-111">Proporcione el control directo del lector.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="5e0ed-112">**SCardGetAttrib**</span><span class="sxs-lookup"><span data-stu-id="5e0ed-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="5e0ed-113">Obtiene los atributos del lector.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="5e0ed-114">**SCardSetAttrib**</span><span class="sxs-lookup"><span data-stu-id="5e0ed-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="5e0ed-115">Establezca el atributo de lector.</span><span class="sxs-lookup"><span data-stu-id="5e0ed-115">Set reader attribute.</span></span>                 |



 

 

 
