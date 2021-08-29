---
description: Filtro del navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro del navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48d4978b31683d99035f6e44ae042f3e982bcde
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983218"
---
# <a name="dvd-navigator-filter"></a>Filtro del navegador de DVD

El filtro DVD Navigator es el filtro de origen de un DVD-Video de filtro de reproducción. Abre todos los archivos necesarios en un volumen de DVD-Video, navega a través de los archivos .vob lineales de DVD-Video y analiza la secuencia de programa MPEG-2 resultante, dividiendo la secuencia en tres pines de salida (vídeo, audio, subpicture).

El filtro DVD Navigator también implementa las interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permiten a una aplicación de reproducción de DVD controlar DVD-Video reproducción.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter,</strong></a> <strong>ISpecifyPropertyPages</strong> | 
| Tipos de medios de pin de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM | 
| Interfaces de pin de entrada | No es aplicable. | 
| Tipos de medios de pin de salida | Tipos base:<br /><ul><li>Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Tipos extendidos:<br /> Vídeo:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>Audio:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>Subimagen:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Para habilitar los tipos extendidos, llame <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>a IDvdControl2::SetOption</strong></a> y establezca <br /> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_DVDNavigator | 
| CLSID de la página de propiedades | No hay ninguna página de propiedades. | 
| Executable | qdvd.dll | 
| <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 




