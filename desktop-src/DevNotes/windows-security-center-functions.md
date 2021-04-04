---
description: Las siguientes funciones se usan con Security Center de Windows.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Funciones de Security Center de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906948"
---
# <a name="windows-security-center-functions"></a><span data-ttu-id="5dfd1-103">Funciones de Security Center de Windows</span><span class="sxs-lookup"><span data-stu-id="5dfd1-103">Windows Security Center Functions</span></span>

<span data-ttu-id="5dfd1-104">Las siguientes funciones se usan con Security Center de Windows.</span><span class="sxs-lookup"><span data-stu-id="5dfd1-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5dfd1-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5dfd1-105">In this section</span></span>



| <span data-ttu-id="5dfd1-106">Tema</span><span class="sxs-lookup"><span data-stu-id="5dfd1-106">Topic</span></span>                                                                           | <span data-ttu-id="5dfd1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dfd1-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dfd1-108">**WscGetSecurityProviderHealth**</span><span class="sxs-lookup"><span data-stu-id="5dfd1-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="5dfd1-109">Obtiene el estado de mantenimiento agregado de las categorías de proveedor de seguridad representadas por los valores de enumeración de [**\_ \_ proveedor de seguridad de WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) especificados.</span><span class="sxs-lookup"><span data-stu-id="5dfd1-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="5dfd1-110">**WscRegisterForChanges**</span><span class="sxs-lookup"><span data-stu-id="5dfd1-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="5dfd1-111">Registra una función de devolución de llamada que se va a ejecutar cuando Windows Security Center (WSC) detecta un cambio que podría afectar al estado de uno de los proveedores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5dfd1-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="5dfd1-112">**WscUnRegisterChanges**</span><span class="sxs-lookup"><span data-stu-id="5dfd1-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="5dfd1-113">Cancela un registro de devolución de llamada realizado por una llamada a la función [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .</span><span class="sxs-lookup"><span data-stu-id="5dfd1-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




