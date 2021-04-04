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
# <a name="windows-deployment-services-structures"></a>Estructuras de servicios de implementación de Windows

Las siguientes estructuras se usan con servicios de implementación de Windows.



| Estructura                                                                         | Descripción                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Dirección de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Especifica la dirección de red de un paquete.                                                                        |
| [**\_mensaje DHCP de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Esta estructura se usa con la API del servidor PXE de servicios de implementación de Windows.                                        |
| [**\_opción DHCP de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Esta estructura se usa con la API del servidor PXE de servicios de implementación de Windows.                                        |
| [**\_proveedor PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Describe un proveedor.                                                                                              |
| [**CRED de la CLI de WDS \_ \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contiene las credenciales usadas para autorizar una sesión de cliente.                                                           |
| [**\_solicitud de TRANSPORTCLIENT de WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Lo utiliza la función [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_información de sesión de TRANSPORTCLIENT \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Lo utiliza la función de devolución de llamada [*pfn \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**\_parámetros de \_ inicialización de TRANSPORTPROVIDER de WDS \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Lo utiliza la función de devolución de llamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**\_configuración de TRANSPORTPROVIDER de WDS \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Lo utiliza la función de devolución de llamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

Lo siguiente está disponible a partir de Windows 8 y Windows Server 2012.

| Estructura                                          | Descripción                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**\_Opción DHCPv6 de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Se usa con la API de servidor PXE de servicios de implementación de Windows. |
| [**\_Mensaje DHCPv6 de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Un mensaje DHCPV6.                                         |



 

 

 




