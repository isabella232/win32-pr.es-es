---
description: Las siguientes funciones se usan para administrar vales de impresión.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Funciones de API de vales de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a908da3aee9e9fa1c3b7181261164860be95193cb4dc0d34a7fe17e6f2a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033923"
---
# <a name="print-ticket-api-functions"></a>Funciones de API de vales de impresión

Las siguientes funciones se usan para administrar vales de impresión.

## <a name="in-this-section"></a>En esta sección



| Función                                                                                  | Descripción                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un vale de impresión.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Convierte un vale de impresión en una [**estructura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Combina dos vales de impresión y devuelve un vale de impresión válido y viable.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Cierra un identificador del proveedor de vales de impresión.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un vale de impresión dentro de [**un IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Convierte un vale de impresión en una [**estructura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Recupera las funciones de la impresora con formato conforme al esquema [de impresión](./printschema.md)XML .<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Recupera las funciones de la impresora del dispositivo con formato conforme al esquema [de impresión](./printschema.md)XML .<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Recupera los recursos de los dispositivos de impresión para una impresora con formato conforme al esquema [de impresión](./printschema.md)XML.<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Combina dos vales de impresión y devuelve un vale de impresión válido y viable.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Abre una instancia de un proveedor de vales de impresión.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Abre una instancia de un proveedor de vales de impresión.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Recupera la versión más alta (más reciente) del esquema [de impresión](./printschema.md) que admite la impresora especificada.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Libera búferes asociados con vales de impresión y funcionalidades de impresión.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Cierra un identificador a un proveedor de vales de impresión.<br/>                                                                                                 |



 

 

