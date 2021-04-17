---
description: 'Las constantes RENDBIND son marcas usadas por el método ITDirectory:: BIND para indicar los tipos de autenticación proporcionados.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes de RENDBIND_ (Rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690697"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="45b3b-103">Constantes de RENDBIND \_</span><span class="sxs-lookup"><span data-stu-id="45b3b-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="45b3b-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="45b3b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="45b3b-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="45b3b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="45b3b-106">Las constantes RENDBIND son marcas usadas por el método [**ITDirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) para indicar los tipos de autenticación proporcionados.</span><span class="sxs-lookup"><span data-stu-id="45b3b-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="45b3b-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**autenticación de RENDBIND \_**</span><span class="sxs-lookup"><span data-stu-id="45b3b-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="45b3b-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b3b-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="45b3b-109">Autenticar al usuario.</span><span class="sxs-lookup"><span data-stu-id="45b3b-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45b3b-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="45b3b-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="45b3b-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b3b-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="45b3b-112">Use el nombre de dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45b3b-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45b3b-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="45b3b-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="45b3b-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="45b3b-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="45b3b-115">Use el nombre de usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45b3b-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45b3b-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="45b3b-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="45b3b-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="45b3b-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="45b3b-118">Usar contraseña predeterminada.</span><span class="sxs-lookup"><span data-stu-id="45b3b-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45b3b-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="45b3b-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="45b3b-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="45b3b-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="45b3b-121">Los tres elementos ORed anteriores juntos para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="45b3b-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45b3b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b3b-122">Requirements</span></span>



| <span data-ttu-id="45b3b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b3b-123">Requirement</span></span> | <span data-ttu-id="45b3b-124">Value</span><span class="sxs-lookup"><span data-stu-id="45b3b-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="45b3b-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="45b3b-125">TAPI version</span></span><br/> | <span data-ttu-id="45b3b-126">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="45b3b-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="45b3b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45b3b-127">Header</span></span><br/>       | <dl> <span data-ttu-id="45b3b-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b3b-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b3b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="45b3b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b3b-130">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="45b3b-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="45b3b-131">**ITDirectory:: Bind**</span><span class="sxs-lookup"><span data-stu-id="45b3b-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




