---
description: En esta sección se describen las estructuras que se usan con la \_ función de escape MXDC y el convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: MXDC estructuras de código de escape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b35c393d00dab227a91cbbb55eeca62039b41ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697690"
---
# <a name="mxdc-escape-code-structures"></a>MXDC estructuras de código de escape

En esta sección se describen las estructuras que se usan con la función de [**\_ escape MXDC**](mxdc-escape.md) y el convertidor de documentos XPS de Microsoft (MXDC).

## <a name="in-this-section"></a>En esta sección



| Estructura                                                                              | Descripción                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MXDC \_ encabezado de escape \_ \_ T**](mxdcescapeheader.md)<br/>                         | La estructura del [**\_ \_ encabezado \_ de escape MXDC**](/windows/desktop/printdocs/mxdcescapeheader) contiene el código de operación para una llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) como el parámetro *nEscape* . También proporciona los tamaños de los búferes de entrada y salida.<br/>  |
| [**MXDC \_ Get \_ filename \_ Data \_ T**](mxdcgetfilenamedata.md)<br/>                 | La estructura [**MXDC \_ Get \_ filename \_ Data \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).<br/>                                                                                                     |
| [**MXDC \_ PRINTTICKET \_ escape \_ T**](mxdcprintticketescape.md)<br/>               | La estructura de [**\_ \_ escape \_ t de MXDC PrintTicket**](mxdcprintticketescape.md) es una estructura de [**encabezado de \_ escape MXDC \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**MXDC \_ PRINTTICKET \_ Data \_ t**](mxdcprintticketpassthrough.md) .<br/>                            |
| [**MXDC \_ datos de PRINTTICKET \_ \_**](mxdcprintticketpassthrough.md)<br/>            | La estructura [**MXDC \_ PRINTTICKET \_ Data \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión y la impresora, para pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.<br/>              |
| [**MXDC \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md)<br/>                             | La estructura [**MXDC \_ S0PAGE \_ Data \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) contiene una página de documento XPS que se pasará al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ T**](mxdcs0pagepassthroughescape.md)<br/> | La estructura [**MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ t**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) es una estructura de [**\_ \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) que se concatena con una estructura [**MXDC \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .<br/>                             |
| [**MXDC \_ S0PAGE \_ de \_ escape de recurso \_ T**](mxdcs0pageresourceescape.md)<br/>       | La estructura de MXDC de los [**\_ \_ recursos S0PAGE \_ \_**](/windows/desktop/printdocs/mxdcs0pageresourceescape) de la estructura t es una estructura de [**encabezado de escape MXDC que se concatena \_ \_ \_**](mxdcescapeheader.md) con una estructura de [**\_ \_ \_ recurso \_ t de MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .<br/>                   |
| [**\_ \_ \_ Recurso T de MXDC XPS S0PAGE \_**](mxdcxpss0pageresource.md)<br/>             | La estructura de [**\_ \_ \_ recursos \_ T de MXDC XPS S0PAGE**](/windows/desktop/printdocs/mxdcxpss0pageresource) contiene información sobre un recurso, como una imagen o fuente, que está asociada a una página de documento XPS y que se va a pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

