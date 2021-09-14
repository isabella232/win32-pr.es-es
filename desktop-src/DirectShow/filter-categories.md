---
description: En las tablas siguientes se muestran los CLID de las DirectShow de filtro.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Categorías de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255147"
---
# <a name="filter-categories"></a>Categorías de filtro

En las tablas siguientes se muestran los CLID de las DirectShow de filtro.

-   [DirectShow Categorías de filtro](#directshow-filter-categories)
-   [Otras categorías de filtro](#other-filter-categories)
-   [DirectShow Meta category de filtro](#directshow-filter-meta-category)
-   [DMO Categorías](#dmo-categories)
-   [Temas relacionados](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Categorías de filtro

El asignador de filtros enumera las categorías [enumeradas aquí.](filter-mapper.md) Sin embargo, de forma predeterminada, el asignador de filtros omite las categorías con los valores DE NO USAR NI USAR NI \_ \_ \_ MENOS. Para obtener más información, [**vea IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Todas las categorías enumeradas aquí también se pueden enumerar con el enumerador [de dispositivos del sistema](system-device-enumerator.md).

Las siguientes categorías se declaran en Uuids.h. Incluya el archivo de encabezado Dshow.h.




| Nombre descriptivo | CLSID | Mérito | 
|---------------|-------|-------|
| Orígenes de captura de audio | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Audio Desafuerciones | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Representadores de audio | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Filtros de control de dispositivos | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow Filtros | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Representadores externos | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Representadores de Midi | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Orígenes de captura de vídeo | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Vídeos desafuerados | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de descompresión de flujos de WDM | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />Esta categoría contiene descodificadores de DVD de hardware.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de captura de streaming de WDM | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de barra cruzada de streaming de WDM | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de representación de streaming de WDM | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos wdm streaming tee/splitter | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de audio de WDM Streaming TV | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivos de tuner de WDM Streaming TV | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Códecs de VBI de streaming de WDM | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

Las siguientes categorías se declaran en el archivo de encabezado Ks.h.



| Nombre descriptivo                          | CLSID                                   | Mérito                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformaciones de comunicación de streaming de WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.** |
| Transformaciones de datos de streaming de WDM          | **KSCATEGORY \_ DATATRANSFORM**           | **NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.** |
| Transformaciones de la interfaz de streaming de WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.** |
| Dispositivos de streaming Mixer WDM            | **MEZCLADOR \_ KSCATEGORY**                   | **NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.** |



 

Las siguientes categorías se declaran en el archivo de encabezado Bdamedia.h. Incluya los siguientes archivos de encabezado: ks.h, ksmedia.h y bdamedia.h.



| Nombre descriptivo                       | CLSID                                       | Mérito                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Proveedores de red BDA               | **PROVEEDOR DE RED \_ KSCATEGORY BDA \_ \_**      | **NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN**       |
| Componentes receptores de BDA             | **KSCATEGORY \_ BDA \_ RECEIVER \_ COMPONENT**    | **NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.** |
| Filtros de representación de BDA               | **RECEPTOR \_ IP KSCATEGORY \_**                    | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |
| Filtros de origen BDA                  | **KSCATEGORY \_ BDA \_ NETWORK \_ TUNER**         | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |
| Representadores de información de transporte BDA | **INFORMACIÓN DE TRANSPORTE \_ DE KSCATEGORY BDA \_ \_** | **NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN**       |



 

> [!Note]  
> Los descodificadores se registran en la categoría "DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Otras categorías de filtro

Las categorías enumeradas aquí se pueden enumerar con el enumerador de dispositivos del sistema, pero no son visibles para el Asignador de filtros y no las usa [Intelligent Conectar](intelligent-connect.md).

Las siguientes categorías se declaran en el archivo de encabezado Qedit.h.



| Nombre descriptivo            | CLID                             | Mérito                   |
|--------------------------|----------------------------------|-------------------------|
| Efectos de vídeo (1 entrada)  | **CLSID \_ VideoEffects1Category** | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |
| Efectos de vídeo (2 entradas) | **CLSID \_ VideoEffects2Category** | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |



 

Estas categorías contienen efectos de vídeo y transiciones [para DirectShow Editing Services](directshow-editing-services.md):

-   "Efectos de vídeo (1 entrada)" contiene efectos de vídeo.
-   "Efectos de vídeo (2 entradas)" contiene transiciones de vídeo.

Para obtener más información, [vea Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).

Las siguientes categorías se declaran en el archivo de encabezado Uuids.h. Incluya el archivo de encabezado Dshow.h.



| Nombre descriptivo       | CLID                                | Mérito                   |
|---------------------|-------------------------------------|-------------------------|
| Codificadores encAPI     | **CLSID \_ MediaEncoderCategory**     | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |
| Multiplexores de EncAPI | **CLSID \_ MediaMultiplexerCategory** | **NO USE EL VALOR DE NO \_ \_ \_ USE.** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Filtro Meta-Category



| Nombre descriptivo                 | CLSID                            | Mérito          |
|-------------------------------|----------------------------------|----------------|
| Categorías de filtro de ActiveMovie | **CLSID \_ ActiveMovieCategories** | No aplicable |



 

Esta meta-categoría contiene una lista de categorías de filtro. Si una categoría de filtro no [](filter-mapper.md) aparece en esta lista, el Asignador de filtros omite la categoría, lo que significa que el filtro no está disponible para [Intelligent Conectar](intelligent-connect.md).

Para enumerar la lista de categorías de filtro, llame a [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el valor CLSID \_ ActiveMovieCategories. Los monikers devueltos por este método admiten las siguientes propiedades.



| Nombre de la propiedad  | Descripción                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| "FriendlyName" | Nombre de categoría (VT \_ BSTR).                                                              |
| "Porción"        | Categoría de categoría (VT \_ I4). Si esta propiedad no está presente, trátese **como NO \_ \_ USE \_ .** |
| "CLSID"        | ClSID de categoría (VT \_ BSTR).                                                             |



 

Para agregar una nueva categoría de filtro a esta lista, llame a [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Categorías

Los objetos multimedia (DMO) de DirectX usan un mecanismo de enumeración diferente de DirectShow filtros. Para obtener más información, [vea Registrar un DMO](registering-a-dmo.md). Sin embargo, puede usar el enumerador de dispositivos del sistema para enumerar DMO categorías. Los monikers se enlazan al filtro [DMO contenedor](dmo-wrapper-filter.md) e inicializan automáticamente el filtro con el DMO.

Además, algunas de las categorías de DMO se asignan a DirectShow de filtro para fines de conexión inteligente:



| DMO Categoría                    | DirectShow Equivalente              |
|---------------------------------|------------------------------------|
| **CODIFICADOR DE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ AudioCompressorCategory** |
| **DESCODIFICADOR DE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **CODIFICADOR DE VÍDEO DMOCATEGORY \_ \_** | **CLSID \_ VideoCompressorCategory** |
| **DESCODIFICADOR DE \_ VÍDEO DMOCATEGORY \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Tenga en cuenta que las categorías de efecto de vídeo y efecto de audio no están asignadas a ninguna DirectShow categorías.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Inteligencia Conectar](intelligent-connect.md)
</dt> <dt>

[Diseño de las claves del Registro](layout-of-the-registry-keys.md)
</dt> <dt>

[Uso del asignador de filtros](using-the-filter-mapper.md)
</dt> <dt>

[Uso del enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




