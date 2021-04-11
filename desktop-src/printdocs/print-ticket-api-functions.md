---
description: Las funciones siguientes se usan para administrar los vales de impresión.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Funciones de la API Print ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910794"
---
# <a name="print-ticket-api-functions"></a>Funciones de la API Print ticket

Las funciones siguientes se usan para administrar los vales de impresión.

## <a name="in-this-section"></a>En esta sección



| Función                                                                                  | Descripción                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en una solicitud de impresión.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Convierte una solicitud de impresión en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Cierra un identificador de proveedor de entradas de impresión.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un vale de impresión dentro de una [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Convierte una solicitud de impresión en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Recupera las capacidades de la impresora con el formato de compatibilidad con el [esquema de impresión](./printschema.md)Xml.<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Recupera las capacidades de la impresora del dispositivo con el formato de compatibilidad con el [esquema de impresión](./printschema.md)Xml.<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Recupera los recursos de dispositivos de impresión de una impresora con el formato compatible con el [esquema de impresión](./printschema.md)Xml.<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Abre una instancia de un proveedor de entradas de impresión.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Abre una instancia de un proveedor de entradas de impresión.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Recupera la versión más alta (la más reciente) del [esquema de impresión](./printschema.md) que admite la impresora especificada.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Libera los búferes asociados a las capacidades de impresión y de impresión.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Cierra un identificador de un proveedor de entradas de impresión.<br/>                                                                                                 |



 

 

