---
description: Esta sección contiene una lista alfabética de las funciones de dispositivo de línea disponibles en el SPI de telefonía.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funciones de dispositivo de línea de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52282154e99ca4e400f6b2d5f32d00a19d62cfe98f0b789d4ee24b9a240293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403715"
---
# <a name="tspi-line-device-functions"></a>Funciones de dispositivo de línea de TSPI

Esta sección contiene una lista alfabética de las funciones de dispositivo de línea disponibles en el SPI de telefonía. La información de cada función incluye lo siguiente:

-   Instrucción del propósito de la función.
-   Sintaxis correcta para la función.
-   Descripción de los parámetros de la función, incluidos los estados de llamada válidos.
-   Descripción del valor devuelto de la función.
-   Una sección Comentarios que puede incluir cualquiera o todas las siguientes: una lista de los estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud; una descripción de los miembros de estructuras de datos grandes que debe rellenar el proveedor de servicios y qué miembros deben conservar intactos sus valores. y la comparación con una función correspondiente dentro de TAPI.
-   Referencias a otras funciones, mensajes o estructuras de datos.
    > [!Note]  
    > Los estados reales en los que se puede realizar una función pueden estar limitados por las funcionalidades del proveedor de servicios. Los proveedores de servicios deben establecer el miembro **dwCallFeatures** en la estructura [**LINECALLSTATUS,**](/windows/win32/api/tapi/ns-tapi-linecallstatus) el **miembro dwAddressFeatures** en la estructura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) y el miembro **dwLineFeatures** de la estructura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) para indicar a las aplicaciones si se permite o no una función en ese momento.

     

Esta sección contiene las siguientes funciones de dispositivo de línea TSPI:

-   [**Línea \_ TSPIAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**Línea \_ TSPIAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**Línea de \_ TSPIAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**Línea \_ TSPIBlindTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**Línea \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**Línea \_ TSPICompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**Línea \_ TSPICompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**Línea \_ TSPIConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**Línea \_ TSPIConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**Línea \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**Línea \_ TSPIDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**Línea \_ TSPIDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**Línea de \_ TSPIDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**Línea \_ TSPIDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [Línea \_ TSPIDropNoOwner](tspi-linedropnoowner.md)
-   [Línea \_ TSPIDropOnClose](tspi-linedroponclose.md)
-   [**Línea \_ TSPIForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**Línea \_ TSPIGatherDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**Línea \_ TSPIGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**Línea \_ TSPIGenerateTone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**Línea \_ TSPIGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**Línea \_ TSPIGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**Línea \_ TSPIGetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**Línea \_ TSPIGetCallIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**Línea \_ TSPIGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**Línea \_ TSPIGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**Línea \_ TSPIGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**Línea \_ TSPIGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ lineGetExtensionID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**LineGetIcon de TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**Línea \_ TSPIGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**\_LineGetNumAddressIDs de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**Línea \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**Línea \_ TSPIMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**Línea \_ TSPIMonitorMedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**Línea de \_ TSPIMonitorMonitorMonitor**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**Línea \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**Línea \_ TSPINegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**Línea \_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**Línea \_ TSPIAbrir**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**LinePickup de TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**Línea \_ TSPIPrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**Línea \_ TSPIReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**Línea \_ TSPIRedirect**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**Línea \_ TSPIReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**Línea \_ TSPIRemoveFromConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ lineSecureCall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**Línea \_ TSPISelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**Línea de \_ TSPISendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**Línea \_ TSPISetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**Línea \_ TSPISetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**Línea \_ TSPISetCallParams**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**Línea \_ TSPISetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**Línea \_ TSPISetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [TSPI \_ lineSetCurrentLocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**Línea \_ TSPISetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ lineSetMediaControl**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**LineSetMediaMode de TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**\_LineSetStatusMessages de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**Línea \_ TSPISetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**Línea \_ TSPISetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**Línea de \_ TSPISwapHold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**Línea \_ TSPIUncompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**Línea \_ TSPIUnhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**Línea \_ TSPIUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
