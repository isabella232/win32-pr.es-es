---
description: Los certificados de cliente y de servidor deben almacenarse en un almacén de certificados al que pueda acceder el proceso de aplicación.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082403"
---
# <a name="certificate-stores"></a><span data-ttu-id="9a871-103">Almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="9a871-103">Certificate Stores</span></span>

<span data-ttu-id="9a871-104">Los certificados de [*cliente*](/windows/desktop/SecGloss/c-gly) y de [*servidor*](/windows/desktop/SecGloss/s-gly) deben almacenarse en un [*almacén de certificados*](/windows/desktop/SecGloss/c-gly) al que pueda acceder el proceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a871-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="9a871-105">Normalmente, se trata de la tienda My, también conocida como el almacén personal.</span><span class="sxs-lookup"><span data-stu-id="9a871-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="9a871-106">Las aplicaciones cliente como Internet Explorer suelen usar el almacén My del usuario actual, mientras que los servidores como Internet Information Services (IIS) usan el almacén del sistema My del equipo local.</span><span class="sxs-lookup"><span data-stu-id="9a871-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="9a871-107">El almacén raíz y el almacén de la [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) se usan cuando Schannel o una aplicación compilan una cadena de certificados que se va a enviar al equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="9a871-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="9a871-108">Estos almacenes se usan para validar una cadena de certificados recibida.</span><span class="sxs-lookup"><span data-stu-id="9a871-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="9a871-109">Para obtener más información, vea [realizar la autenticación con Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="9a871-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
