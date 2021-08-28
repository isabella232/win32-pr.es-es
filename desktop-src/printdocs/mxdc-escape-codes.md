---
description: En esta sección se describen las estructuras que se usan con la función ESCAPE de MXDC y el Convertidor \_ de documentos XPS de Microsoft (MXDC).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Estructuras de código de escape de MXDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b87ef962be9f8fffa1ae0b2d126cecfda4cc157118f4defd21360b030dc9d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948395"
---
# <a name="mxdc-escape-code-structures"></a>Estructuras de código de escape de MXDC

En esta sección se describen las estructuras que se usan con la función [**\_ ESCAPE de MXDC**](mxdc-escape.md) y microsoft XPS Document Converter (MXDC).

## <a name="in-this-section"></a>En esta sección



| Estructura                                                                              | Descripción                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCABEZADO DE ESCAPE DE MXDC \_ \_ \_ T**](mxdcescapeheader.md)<br/>                         | La [**estructura MXDC \_ ESCAPE HEADER \_ \_ T**](/windows/desktop/printdocs/mxdcescapeheader) contiene el código de operación de una llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ ESCAPE**](mxdc-escape.md) como parámetro *nEscape.* También proporciona los tamaños de los búferes de entrada y salida.<br/>  |
| [**MXDC \_ GET \_ FILENAME \_ DATA \_ T**](mxdcgetfilenamedata.md)<br/>                 | La [**estructura MXDC \_ GET FILENAME \_ DATA \_ \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del Convertidor de documentos DE Microsoft XPS (MXDC).<br/>                                                                                                     |
| [**MXDC \_ PRINTTICKET \_ ESCAPE \_ T**](mxdcprintticketescape.md)<br/>               | La [**estructura MXDC \_ PRINTTICKET ESCAPE \_ \_ T**](mxdcprintticketescape.md) es una estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**\_ MXDC PRINTTICKET \_ DATA \_ T.**](mxdcprintticketpassthrough.md)<br/>                            |
| [**MXDC \_ PRINTTICKET \_ DATA \_ T**](mxdcprintticketpassthrough.md)<br/>            | La estructura [**MXDC \_ PRINTTICKET \_ DATA \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión e impresora, para pasar al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.<br/>              |
| [**MXDC \_ S0PAGE \_ DATA \_ T**](mxdcs0pagedata.md)<br/>                             | La [**estructura MXDC \_ S0PAGE \_ DATA \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) contiene una página de documento XPS que se pasará al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ PASSTHROUGH \_ ESCAPE \_ T**](mxdcs0pagepassthroughescape.md)<br/> | La [**estructura MXDC \_ S0PAGE \_ PASSTHROUGH ESCAPE \_ \_ T**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) es una estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**DATA \_ \_ \_ T de MXDC S0PAGE.**](mxdcs0pagedata.md)<br/>                             |
| [**MXDC \_ S0PAGE \_ RESOURCE \_ ESCAPE \_ T**](mxdcs0pageresourceescape.md)<br/>       | La [**estructura MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T**](/windows/desktop/printdocs/mxdcs0pageresourceescape) es una estructura T DE ENCABEZADO DE ESCAPE DE [**MXDC \_ \_ \_**](mxdcescapeheader.md) concatenada con una estructura T de RECURSOS [**\_ \_ S0PAGE \_ \_ de MXDC XPS.**](mxdcxpss0pageresource.md)<br/>                   |
| [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T**](mxdcxpss0pageresource.md)<br/>             | La estructura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T**](/windows/desktop/printdocs/mxdcxpss0pageresource) contiene información sobre un recurso, como una imagen o fuente, que está asociado a una página de documento XPS y se va a pasar al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

