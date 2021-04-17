---
description: El conjunto de propiedades protección de copia de DVD proporciona autenticación de la información de protección de copia de los descifrados de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-video grabado previamente.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propiedades de protección de copia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680922"
---
# <a name="dvd-copy-protection-property-set"></a>Conjunto de propiedades de protección de copia de DVD

El conjunto de propiedades protección de copia de DVD proporciona autenticación de la información de protección de copia de los descifrados de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-video grabado previamente.

Microsoft proporciona software que facilita el proceso de autenticación requerido por el esquema de cifrado, lo que permite que una unidad de DVD-ROM autentique y transfiera claves con un DVD Decrypter. Microsoft no tiene planes actuales para enviar un DVD Decrypter y, en su lugar, proporciona código del sistema operativo que actuará como agente para habilitar la autenticación de los descifrados de hardware o software.

El navegador de DVD inicia y controla el proceso de intercambio de claves. El minicontrolador de DVD solo tiene que implementar las siguientes propiedades. Otros componentes controlan el resto.

Cada flujo de entrada de DVD recibirá las propiedades de protección contra copia. Esto es así incluso si el mismo hardware controla todos los flujos de DVD.

La siguiente información presenta las constantes y los tipos de datos necesarios para usar en esta propiedad establecida en llamadas a métodos [**IKsPropertySet**](ikspropertyset.md) . Proporciona valores para los parámetros **GUID** (*GUIDPROPSET*), ID. de propiedad (*dwPropID*) y tipo de datos de propiedad (*pPropData*).



|                   |                           |
|-------------------|---------------------------|
| GUID del conjunto de propiedades | \_CopyProt KSPROPSETID \_ AM |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Id. de propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></td>
<td>Consulta si la salida de vídeo es una definición estándar, vídeo de componente analógico.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Esta es una propiedad de solo conjunto. Esta propiedad establece el nivel de protección de copia analógica del codificador NTSC en el extremo de salida del PIN receptor. Utiliza <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>En esta propiedad se admiten las operaciones GET y set. Una operación Get solicita al descodificador que proporcione su clave de desafío de bus. Una operación SET proporciona el descodificador con la clave de desafío de bus de la unidad de DVD. Los datos pasados en esta propiedad serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Se trata de una propiedad de solo obtención. Esta propiedad solicita que la clave de bus 2 del descodificador se transfiera a la unidad de DVD. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Propiedad de solo establecimiento. Esto proporciona la clave de disco. La clave es una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Esta es una propiedad de solo conjunto. Esta propiedad proporciona la clave 1 del bus de unidad de DVD al descodificador. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>El código de región solicita la definición de la región en la que el descodificador puede reproducirse tal y como se define en el consorcio de DVD. Esta región se define como una estructura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>En esta propiedad se admiten get y set. Primero se llama a get para determinar si se requiere autenticación. Las propiedades establecidas son indicaciones sobre la fase de negociación de la protección de copia que el filtro está entrando. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Si esta propiedad es <strong>true</strong>, el explorador de DVD no envía <strong>AM_UseNewCSSKey</strong> muestras antes de negociar la clave de disco. Vea <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Solo lectura. Los datos de la propiedad son un valor <strong>booleano</strong> .<br/>
<blockquote>
[!Note]<br />
Se aplica a Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Esta es una propiedad de solo conjunto. Esto proporciona la clave de título del contenido actual. La clave es una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




