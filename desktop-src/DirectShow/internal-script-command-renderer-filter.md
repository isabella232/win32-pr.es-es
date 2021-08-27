---
description: Filtro de representador de comandos de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de representador de comandos de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982218"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro de representador de comandos de script interno

Recibe comandos de script y los envía a la aplicación.

Este filtro acepta comandos de script en uno de estos dos formatos:

-   Texto \_ MEDIATYPE: cada ejemplo multimedia contiene una cadena de texto ANSI.
-   MEDIATYPE \_ ScriptCommand: cada ejemplo multimedia contiene dos cadenas Unicode terminadas en NULL, concatenadas juntas. La primera cadena describe el tipo de comando y la segunda cadena es el comando de script.

    Cuando el filtro recibe un ejemplo, envía una notificación [**de eventos OLE EVENT \_ \_ de EC.**](ec-ole-event.md) El primer parámetro de evento es **un BSTR** con el tipo de comando o `Text` si el formato es MEDIATYPE \_ Text. El segundo parámetro de evento es **un BSTR** con el comando de script. La aplicación puede recuperar el evento y responder al comando de script.

Para obtener un ejemplo de cómo usar este filtro, vea [Analizador de SAMI (CC).](sami--cc--parser-filter.md)




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | 
| Tipos de medios de pin de entrada | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | No es aplicable | 
| Interfaces de pin de salida | No es aplicable | 
| Filtrar CLSID | {48025243-2D39-11CE-875D-00608CB78066} | 
| CLSID de la página de propiedades | Ninguna página de propiedades | 
| Executable | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



