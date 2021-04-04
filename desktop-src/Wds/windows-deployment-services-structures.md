---
title: Estructuras de servicios de implementación de Windows
description: Las siguientes estructuras se usan con servicios de implementación de Windows.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076220"
---
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="b4b3f-103">Estructuras de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="b4b3f-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="b4b3f-104">Las siguientes estructuras se usan con servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="b4b3f-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="b4b3f-105">Structure</span></span>                                                                         | <span data-ttu-id="b4b3f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4b3f-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4b3f-107">**Dirección de PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="b4b3f-108">Especifica la dirección de red de un paquete.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="b4b3f-109">**\_mensaje DHCP de PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="b4b3f-110">Esta estructura se usa con la API del servidor PXE de servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="b4b3f-111">**\_opción DHCP de PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="b4b3f-112">Esta estructura se usa con la API del servidor PXE de servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="b4b3f-113">**\_proveedor PXE**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="b4b3f-114">Describe un proveedor.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="b4b3f-115">**CRED de la CLI de WDS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="b4b3f-116">Contiene las credenciales usadas para autorizar una sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="b4b3f-117">**\_solicitud de TRANSPORTCLIENT de WDS \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="b4b3f-118">Lo utiliza la función [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="b4b3f-119">**\_información de sesión de TRANSPORTCLIENT \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="b4b3f-120">Lo utiliza la función de devolución de llamada [*pfn \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="b4b3f-121">**\_parámetros de \_ inicialización de TRANSPORTPROVIDER de WDS \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="b4b3f-122">Lo utiliza la función de devolución de llamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="b4b3f-123">**\_configuración de TRANSPORTPROVIDER de WDS \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="b4b3f-124">Lo utiliza la función de devolución de llamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="b4b3f-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="b4b3f-125">Lo siguiente está disponible a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="b4b3f-126">Estructura</span><span class="sxs-lookup"><span data-stu-id="b4b3f-126">Structure</span></span>                                          | <span data-ttu-id="b4b3f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4b3f-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="b4b3f-128">**\_Opción DHCPv6 de PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="b4b3f-129">Se usa con la API de servidor PXE de servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="b4b3f-130">**\_Mensaje DHCPv6 de PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b4b3f-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="b4b3f-131">Un mensaje DHCPV6.</span><span class="sxs-lookup"><span data-stu-id="b4b3f-131">A DHCPV6 message.</span></span>                                         |



 

 

 




