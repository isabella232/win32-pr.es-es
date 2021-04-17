---
description: La lista siguiente contiene los métodos internos de la dirección CMSP.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Métodos auxiliares internos de CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689556"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="05036-103">Métodos auxiliares internos de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="05036-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="05036-104">Métodos auxiliares internos de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="05036-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="05036-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="05036-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05036-106">**GetStaticTerminals**</span><span class="sxs-lookup"><span data-stu-id="05036-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="05036-107">Lo llama [**Get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) y [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) para obtener una matriz de terminales estáticas que se pueden usar en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="05036-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="05036-108">**GetDynamicTerminalClasses**</span><span class="sxs-lookup"><span data-stu-id="05036-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="05036-109">Lo llama [**Get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) y [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) para obtener una matriz de clases de terminal dinámicas que se pueden usar en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="05036-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="05036-110">**UpdateTerminalList**</span><span class="sxs-lookup"><span data-stu-id="05036-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="05036-111">Rellena la lista de terminales estáticas del MSP.</span><span class="sxs-lookup"><span data-stu-id="05036-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="05036-112">**ReceiveTSPAddressData**</span><span class="sxs-lookup"><span data-stu-id="05036-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="05036-113">Se llama cuando un mensaje de datos de TSP está diseñado para ser procesado por la dirección en lugar de por una llamada específica.</span><span class="sxs-lookup"><span data-stu-id="05036-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="05036-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05036-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05036-115">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="05036-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
