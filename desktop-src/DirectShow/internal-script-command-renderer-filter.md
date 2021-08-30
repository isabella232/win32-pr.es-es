---
description: Filtro de representador de comandos de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de representador de comandos de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833c8b1034277019bfcaf222f78ab00a5c2cc8a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478881"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro de representador de comandos de script interno

Recibe comandos de script y los envía a la aplicación.

Este filtro acepta comandos de script en uno de estos dos formatos:

-   Texto \_ MEDIATYPE: cada ejemplo multimedia contiene una cadena de texto ANSI.
-   MEDIATYPE \_ ScriptCommand: cada ejemplo multimedia contiene dos cadenas Unicode terminadas en NULL, concatenadas juntas. La primera cadena describe el tipo de comando y la segunda cadena es el comando de script.

    Cuando el filtro recibe un ejemplo, envía una notificación [**de eventos EC OLE \_ \_ EVENT.**](ec-ole-event.md) El primer parámetro de evento es **un BSTR** con el tipo de comando o si `Text` el formato es TEXTO \_ MEDIATYPE. El segundo parámetro de evento es **un BSTR** con el comando de script. La aplicación puede recuperar el evento y responder al comando de script.

Para obtener un ejemplo de cómo usar este filtro, vea [Analizador SAMI (CC).](sami--cc--parser-filter.md)




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | Tipos de medios de pin de entrada | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de anclar salida | No aplicable | | Interfaces de pin de salida | No aplicable | | Filtrar clsid | {48025243-2D39-11CE-875D-00608CB78066} | | ClSID de página de propiedades | Ninguna página de propiedades | | Archivos ejecutables | Quartz.dll | | <a href="merit.md">Ventajas |</a> MERIT_PREFERRED + 1 | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



