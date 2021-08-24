---
title: Windows Estructuras de Deployment Services
description: Las estructuras siguientes se usan con Windows Deployment Services.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760255"
---
# <a name="windows-deployment-services-structures"></a>Windows Estructuras de Deployment Services

Las estructuras siguientes se usan con Windows Deployment Services.



| Estructura                                                                         | Descripción                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**DIRECCIÓN \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Especifica la dirección de red de un paquete.                                                                        |
| [**MENSAJE \_ DHCP PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Esta estructura se usa con la API de servidor PXE Windows Deployment Services.                                        |
| [**OPCIÓN \_ DHCP PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Esta estructura se usa con la API de servidor PXE Windows Deployment Services.                                        |
| [**PROVEEDOR \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Describe un proveedor.                                                                                              |
| [**CRED de \_ la CLI de WDS \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contiene las credenciales usadas para autorizar una sesión de cliente.                                                           |
| [**SOLICITUD \_ TRANSPORTCLIENT DE WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Usado por la [**función WdsTransportClientStartSession.**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)                     |
| [**INFORMACIÓN DE LA \_ SESIÓN DE \_ TRANSPORTCLIENT**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Usado por la función de devolución de [*llamada \_ PFN WdsTransportClientSessionStartEx.*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) |
| [**PARAMS \_ DE \_ INIT DE WDS TRANSPORTPROVIDER \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Usado por la [**función de devolución de llamada WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |
| [**CONFIGURACIÓN DE TRANSPORTPROVIDER DE WDS \_ \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Usado por la [**función de devolución de llamada WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |



 

Lo siguiente está disponible a partir de Windows 8 y Windows Server 2012.

| Estructura                                          | Descripción                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**OPCIÓN \_ DHCPV6 de PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Se usa con Windows DEPLOYMENT Services PXE Server API. |
| [**MENSAJE \_ DHCPV6 DE PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Mensaje DHCPV6.                                         |



 

 

 




