---
description: En las tablas siguientes se enumeran los CLSID de las categorías de filtros de DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Categorías de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422768"
---
# <a name="filter-categories"></a>Categorías de filtro

En las tablas siguientes se enumeran los CLSID de las categorías de filtros de DirectShow.

-   [Categorías de filtros de DirectShow](#directshow-filter-categories)
-   [Otras categorías de filtro](#other-filter-categories)
-   [Metacategoría del filtro de DirectShow](#directshow-filter-meta-category)
-   [Categorías de DMO](#dmo-categories)
-   [Temas relacionados](#related-topics)

## <a name="directshow-filter-categories"></a>Categorías de filtros de DirectShow

Las categorías enumeradas aquí se enumeran mediante el [asignador de filtros](filter-mapper.md). Sin embargo, de forma predeterminada, el asignador de filtros omite las categorías con méritos de mérito \_ \_ no \_ usar o menos. Para obtener más información, vea [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Todas las categorías que se enumeran aquí también se pueden enumerar con el [enumerador de dispositivos del sistema](system-device-enumerator.md).

Las siguientes categorías se declaran en UUID. h. Incluya el archivo de encabezado DShow. h.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre descriptivo</th>
<th>CLSID</th>
<th>Fundament</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Orígenes de captura de audio</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Compresores de audio</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Representadores de audio</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Filtros de control de dispositivo</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Filtros de DirectShow</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Representadores externos</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Representadores MIDI</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Orígenes de captura de vídeo</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Compresores de vídeo</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de descompresión de secuencia WDM</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
Esta categoría contiene descodificadores de DVD de hardware.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de captura de transmisión por secuencias WDM</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de barras cruzadas de transmisión por secuencias WDM</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de representación de transmisión por secuencias WDM</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de transmisión por secuencias WDM/divisora</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivos de audio de TV de transmisión por secuencias WDM</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivos de sintonizador de TV de streaming WDM</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Códecs de streaming VBI WDM</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Las siguientes categorías se declaran en el archivo de encabezado KS. h.



| Nombre descriptivo                          | CLSID                                   | Fundament                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformaciones de comunicación de transmisión por secuencias WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MÉRITO \_ \_ no se \_ usa** |
| Transformaciones de datos de transmisión por secuencias WDM          | **KSCATEGORY ( \_ transformación)**           | **MÉRITO \_ \_ no se \_ usa** |
| Transformaciones de la interfaz de streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MÉRITO \_ \_ no se \_ usa** |
| Dispositivos de mezclador de transmisión por secuencias WDM            | **\_mezclador KSCATEGORY**                   | **MÉRITO \_ \_ no se \_ usa** |



 

Las siguientes categorías se declaran en el archivo de encabezado Bdamedia. h. Incluya los archivos de encabezado siguientes: KS. h, ksmedia. h y bdamedia. h.



| Nombre descriptivo                       | CLSID                                       | Fundament                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Proveedores de redes BDA               | **\_proveedor de \_ red \_ BDA de KSCATEGORY**      | **MÉRITO \_ normal**       |
| Componentes del receptor de BDA             | **\_componente de \_ receptor de BDA de KSCATEGORY \_**    | **MÉRITO \_ \_ no se \_ usa** |
| Filtros de representación de BDA               | **\_receptor de IP de KSCATEGORY \_**                    | **MÉRITO \_ \_ no se \_ usa** |
| Filtros de origen de BDA                  | **\_ \_ sintonizador de red BDA de KSCATEGORY \_**         | **MÉRITO \_ \_ no se \_ usa** |
| Representadores de información de transporte BDA | **\_información de \_ transporte de BDA de KSCATEGORY \_** | **MÉRITO \_ normal**       |



 

> [!Note]  
> Los descodificadores se registran en la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Otras categorías de filtro

Las categorías que se enumeran aquí se pueden enumerar con el enumerador de dispositivos del sistema, pero no son visibles para el asignador de filtros y la [conexión inteligente](intelligent-connect.md)no las usa.

Las siguientes categorías se declaran en el archivo de encabezado QEDIT. h.



| Nombre descriptivo            | CLID                             | Fundament                   |
|--------------------------|----------------------------------|-------------------------|
| Efectos de vídeo (1 entrada)  | **CLSID \_ VideoEffects1Category** | **MÉRITO \_ \_ no se \_ usa** |
| Efectos de vídeo (2 entradas) | **CLSID \_ VideoEffects2Category** | **MÉRITO \_ \_ no se \_ usa** |



 

Estas categorías contienen efectos de vídeo y transiciones para los [servicios de edición de DirectShow](directshow-editing-services.md):

-   "Efectos de vídeo (1 entrada)" contiene efectos de vídeo.
-   "Efectos de vídeo (2 entradas)" contiene transiciones de vídeo.

Para obtener más información, consulte [enumeración de efectos y transiciones](enumerating-effects-and-transitions.md).

Las siguientes categorías se declaran en el archivo de encabezado UUID. h. Incluya el archivo de encabezado DShow. h.



| Nombre descriptivo       | CLID                                | Fundament                   |
|---------------------|-------------------------------------|-------------------------|
| Codificadores de encapi     | **CLSID \_ MediaEncoderCategory**     | **MÉRITO \_ \_ no se \_ usa** |
| Multiplexadores de encapi | **CLSID \_ MediaMultiplexerCategory** | **MÉRITO \_ \_ no se \_ usa** |



 

## <a name="directshow-filter-meta-category"></a>Meta-Category de filtros de DirectShow



| Nombre descriptivo                 | CLSID                            | Fundament          |
|-------------------------------|----------------------------------|----------------|
| Categorías de filtro de ActiveMovie | **CLSID \_ ActiveMovieCategories** | No aplicable |



 

Esta metacategoría contiene una lista de categorías de filtro. Si una categoría de filtro no aparece en esta lista, el [asignador de filtros](filter-mapper.md) omite la categoría, lo que significa que el filtro no está disponible para la [conexión inteligente](intelligent-connect.md).

Para enumerar la lista de categorías de filtro, llame a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el valor CLSID \_ ActiveMovieCategories. Los monikers devueltos por este método admiten las siguientes propiedades.



| Nombre de la propiedad  | Descripción                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Nombre de categoría (VT \_ BSTR).                                                              |
| Fundament        | Mérito de categoría (VT \_ I4). Si esta propiedad está ausente, trate como **mérito \_ \_ no \_ usar**. |
| CLSID        | Categoría CLSID (VT \_ BSTR).                                                             |



 

Para agregar una nueva categoría de filtro a esta lista, llame a [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>Categorías de DMO

Los objetos multimedia de DirectX (DMOs) usan un mecanismo de enumeración diferente de los filtros de DirectShow. Para obtener más información, consulte [registrar un DMO](registering-a-dmo.md). Sin embargo, puede usar el enumerador de dispositivos del sistema para enumerar las categorías de DMO. Los monikers se enlazan al [filtro de contenedor de DMO](dmo-wrapper-filter.md) e inicializan automáticamente el filtro con DMO.

Además, algunas de las categorías de DMO se asignan a las categorías de filtro de DirectShow para la conexión inteligente:



| Categoría de DMO                    | Equivalente de DirectShow              |
|---------------------------------|------------------------------------|
| **\_codificador de audio DMOCATEGORY \_** | **CLSID \_ AudioCompressorCategory** |
| **descodificador de audio de DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **\_codificador de vídeo de DMOCATEGORY \_** | **CLSID \_ VideoCompressorCategory** |
| **descodificador de vídeo de DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Tenga en cuenta que las categorías efecto de vídeo y efecto de audio no están asignadas a ninguna categoría de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> <dt>

[Enumerar dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Conexión inteligente](intelligent-connect.md)
</dt> <dt>

[Diseño de las claves del registro](layout-of-the-registry-keys.md)
</dt> <dt>

[Usar el asignador de filtros](using-the-filter-mapper.md)
</dt> <dt>

[Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




