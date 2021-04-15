---
description: La interfaz IX509EndorsementKey expone las siguientes propiedades.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propiedades de IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648486"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="8ad3a-103">Propiedades de IX509EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="8ad3a-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="8ad3a-104">La interfaz [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="8ad3a-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8ad3a-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8ad3a-105">In this section</span></span>



| <span data-ttu-id="8ad3a-106">Tema</span><span class="sxs-lookup"><span data-stu-id="8ad3a-106">Topic</span></span>                                                                        | <span data-ttu-id="8ad3a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ad3a-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ad3a-108">**Propiedad Length**</span><span class="sxs-lookup"><span data-stu-id="8ad3a-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="8ad3a-109">Longitud de bit de la clave de aprobación.</span><span class="sxs-lookup"><span data-stu-id="8ad3a-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="8ad3a-110">Solo se puede tener acceso a esta propiedad después de llamar al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="8ad3a-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="8ad3a-111">**Propiedad opened**</span><span class="sxs-lookup"><span data-stu-id="8ad3a-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="8ad3a-112">Indica si se ha llamado correctamente al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="8ad3a-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="8ad3a-113">**ProviderName (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="8ad3a-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="8ad3a-114">Nombre del proveedor de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8ad3a-114">The name of the encryption provider.</span></span> <span data-ttu-id="8ad3a-115">El valor predeterminado es el proveedor de criptografía de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8ad3a-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="8ad3a-116">Debe establecer la propiedad [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de llamar al método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="8ad3a-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="8ad3a-117">No se puede cambiar la propiedad **providerName** después de haber llamado al método **Open** .</span><span class="sxs-lookup"><span data-stu-id="8ad3a-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




