---
description: Errores de representación
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495430"
---
# <a name="rendering-errors"></a>Errores de representación

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) define varios códigos de error que se usan para registrar los errores de representación. Si un proyecto no se representa correctamente, el motor de representación llama al método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . En la tabla siguiente se resumen los parámetros proporcionados a **LogError**:

-   El código de error se encuentra en el parámetro *ErrorCode* .
-   La descripción se incluye en el parámetro ErrorString.
-   La descripción se incluye en el parámetro *ErrorString* .
-   Si hay información adicional, el tipo **Variant** se incluye en el miembro **VT** de la **variante** a la que apunta *pExtraInfo*.

> [!Note]  
> Los códigos de error que se describen aquí no son valores **HRESULT** . Para obtener una lista de valores devueltos **HRESULT** específicos de des, vea [códigos de error y de éxito](error-and-success-codes.md).

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de error</th>
<th>Descripción</th>
<th>Información adicional</th>
<th>Tipo Variant</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>El nombre de archivo no existe o DirectShow no reconoce la extensión de archivo.</td>
<td>Nombre de archivo</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>El tipo de archivo no coincide con la extensión de archivo o el archivo está dañado.</td>
<td>Nombre de archivo</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Se necesita el nombre de archivo, pero no se proporcionó.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>No se puede analizar el origen de datos proporcionado por este origen.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>error inesperado. Algunos componentes de DirectShow no están instalados correctamente.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>El filtro de origen no acepta nombres de archivo.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>No se admite el tipo de medio del grupo.</td>
<td>Número de grupo</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Número de secuencia no válido para este origen.</td>
<td>Número de secuencia</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Memoria insuficiente</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Un mapa de bits de la secuencia no es del mismo tipo que los demás.</td>
<td>Nombre del mapa de bits</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Las horas de medios del clip no son válidas o la secuencia de mapa de bits independiente del dispositivo (DIB) es demasiado corta.
<blockquote>
[!Note]<br />
Si se producen otros errores de representación, este error puede producirse aunque las horas de los medios sean válidas.
</blockquote>
<br/></td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>El identificador de clase (CLSID) del efecto o la transición no es válido.</td>
<td>CLSID</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>El CLSID del efecto o transición predeterminados no es válido.</td>
<td>CLSID</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Su versión de DirectX no admite transiciones tridimensionales.</td>
<td>CLSID</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Este efecto no es el tipo correcto o está roto.</td>
<td>CLSID</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>No existe ninguna propiedad de este tipo en el objeto.</td>
<td>Nombre de propiedad</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valor no válido para esta propiedad.</td>
<td>Valor especificado</td>
<td><strong>VARIANTE</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Error de sintaxis en el archivo XML.</td>
<td>Número de línea</td>
<td>VT_I4 (entero de 4 bytes)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>No se puede encontrar el filtro especificado en XML por categoría e instancia.</td>
<td>Nombre descriptivo (instancia)</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Error al escribir el archivo XML en el disco.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID no es un filtro válido de efecto de audio de DirectShow.</td>
<td>CLSID</td>
<td><strong>UTILICEN</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>No se puede encontrar un compresor para generar el formato de compresión especificado.</td>
<td>None</td>
<td>No aplicable</td>
</tr>
</tbody>
</table>



 

Nunca deben producirse los siguientes errores. Si encuentra alguno de estos errores, envíe un informe de errores a Microsoft.



| Código de error                 | Descripción                                 |
|----------------------------|---------------------------------------------|
| \_análisis de \_ escala de tiempo de IDENTIFICADOres DEX \_  | Error inesperado al analizar la escala de tiempo.      |
| \_error de gráfico de identificadores DEX \_ \_     | Error inesperado al compilar el gráfico de filtro. |
| ERROR de la \_ cuadrícula de identificadores DEX \_ \_      | Error inesperado con la cuadrícula interna.    |
| ERROR de la \_ interfaz de identificadores DEX \_ \_ | Error inesperado al obtener una interfaz.      |



 

 

 




