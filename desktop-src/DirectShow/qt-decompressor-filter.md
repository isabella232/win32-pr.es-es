---
description: Filtro de descompresión QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompresión QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983658"
---
# <a name="qt-decompressor-filter"></a>Filtro de descompresión QT

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

El filtro de descompresión QT descomprime apple® quicktime® vídeo 2.0. Este formato se usa normalmente en archivos QuickTime antiguos.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipos de medios de pin de entrada | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_QTDec | 
| CLSID de la página de propiedades | No hay ninguna página de propiedades. | 
| Executable | quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




