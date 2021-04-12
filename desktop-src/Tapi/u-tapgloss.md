---
description: Los siguientes términos son útiles para comprender la tecnología de TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 465b8ff4-4622-4638-9c5a-102a43afad6f
title: U (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72372c7070ab0f8f1cca27e5c92b38594fcef64f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361201"
---
# <a name="u-telephony-api"></a><span data-ttu-id="d34e6-103">U (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="d34e6-103">U (Telephony API)</span></span>

<span data-ttu-id="d34e6-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N o [p](p-tapgloss.md) Q [R](r-tapgloss.md) [s](s-tapgloss.md) [T](t-tapgloss.md) U [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d34e6-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) U [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d34e6-105"><span id="tapi2.unimodem_tapgloss"></span><span id="TAPI2.UNIMODEM_TAPGLOSS"></span>**UniModem**</span><span class="sxs-lookup"><span data-stu-id="d34e6-105"><span id="tapi2.unimodem_tapgloss"></span><span id="TAPI2.UNIMODEM_TAPGLOSS"></span>**UniModem**</span></span>
</dt> <dd>

<span data-ttu-id="d34e6-106">El controlador de módem universal en TAPI.</span><span class="sxs-lookup"><span data-stu-id="d34e6-106">The universal modem driver in TAPI.</span></span> <span data-ttu-id="d34e6-107">Unimodem es un componente de nivel de controlador que utiliza archivos de Descripción del módem para controlar su interacción con el controlador de comunicaciones, VCOMM.</span><span class="sxs-lookup"><span data-stu-id="d34e6-107">UniModem is a driver-level component that uses modem description files to control its interaction with the communications driver, VCOMM.</span></span> <span data-ttu-id="d34e6-108">Vea [*VCOMM*](v-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="d34e6-108">See [*VCOMM*](v-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="d34e6-109"><span id="tapi2.user_user_information_tapgloss"></span><span id="TAPI2.USER_USER_INFORMATION_TAPGLOSS"></span>**información de usuario**</span><span class="sxs-lookup"><span data-stu-id="d34e6-109"><span id="tapi2.user_user_information_tapgloss"></span><span id="TAPI2.USER_USER_INFORMATION_TAPGLOSS"></span>**user-user information**</span></span>
</dt> <dd>

<span data-ttu-id="d34e6-110">Información que se envía de un usuario a otro por la estación remota (ISDN).</span><span class="sxs-lookup"><span data-stu-id="d34e6-110">Information that is sent from one user to another by the remote station (ISDN).</span></span> <span data-ttu-id="d34e6-111">Para información adicional:</span><span class="sxs-lookup"><span data-stu-id="d34e6-111">For additional information:</span></span>

<span data-ttu-id="d34e6-112">**TAPI 2. x:** Vea [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo), [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="d34e6-112">**TAPI 2.x:** See [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo), [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo).</span></span>

<span data-ttu-id="d34e6-113">**TSPI:** Consulte [**TSPI \_ lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo), [**TSPI \_ lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="d34e6-113">**TSPI:** See [**TSPI\_lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo), [**TSPI\_lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo).</span></span>

<span data-ttu-id="d34e6-114">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer), [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo).</span><span class="sxs-lookup"><span data-stu-id="d34e6-114">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer), [**ITCallInfo::put\_CallInfoBuffer**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/win32/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo).</span></span>

</dd> </dl>

 

 
