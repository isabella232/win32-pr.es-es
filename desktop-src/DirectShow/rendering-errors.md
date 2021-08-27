---
description: Errores de representación
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5af72ccf7ca76b2d4899178757282f1879c06052d2db2f3e1d929ddeef0f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050615"
---
# <a name="rendering-errors"></a>Errores de representación

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) define varios códigos de error que se usan para registrar errores de representación. Si un proyecto no se representa correctamente, el motor de representación llama al [**método IAMErrorLog::LogError.**](iamerrorlog-logerror.md) En la tabla siguiente se resumen los parámetros dados a **LogError**:

-   El código de error está incluido en el *parámetro ErrorCode.*
-   La descripción está contenida en el parámetro ErrorString.
-   La descripción está contenida en el *parámetro ErrorString.*
-   Si hay información adicional, el tipo **VARIANT** se encuentra en el miembro **vt** de **variant** al que apunta *pExtraInfo*.

> [!Note]  
> Los códigos de error que se describen aquí no son **valores HRESULT.** Para obtener una lista de **valores devueltos HRESULT** específicos de DES, vea [Códigos de error y correctos.](error-and-success-codes.md)

 



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
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>El tipo de archivo no coincide con la extensión de archivo o el archivo está dañado.</td>
<td>Nombre de archivo</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>El nombre de archivo era necesario, pero no se ha especificado.</td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>No se puede analizar el origen de datos proporcionado por este origen.</td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>error inesperado. Algunos DirectShow componente no están instalados correctamente.</td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>El filtro de origen no acepta nombres de archivo.</td>
<td>Ninguno</td>
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
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Un mapa de bits de la secuencia no era del mismo tipo que los demás.</td>
<td>Nombre del mapa de bits</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Los tiempos de medios del clip no son válidos o la secuencia de mapa de bits independiente del dispositivo (DIB) es demasiado corta.
<blockquote>
[!Note]<br />
Si se producen otros errores de representación, este error puede producirse aunque los tiempos de los medios sean válidos.
</blockquote>
<br/></td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>El identificador de clase (CLSID) del efecto o la transición no es válido.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>El CLSID del efecto o transición predeterminados no es válido.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>La versión de DirectX no admite transiciones tridimensionales.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Este efecto no es el tipo correcto o está roto.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>No existe ninguna propiedad de este tipo en el objeto .</td>
<td>Nombre de propiedad</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valor no válido para esta propiedad.</td>
<td>Valor especificado</td>
<td><strong>Variante</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Error de sintaxis en el archivo XML.</td>
<td>Número de línea</td>
<td>VT_I4 (entero de 4 bytes)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>No se encuentra el filtro especificado en XML por categoría e instancia.</td>
<td>Nombre descriptivo (instancia)</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Error al escribir el archivo XML en el disco.</td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID no es un filtro DirectShow efecto de audio válido.</td>
<td>CLSID</td>
<td><strong>Bstr</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>No se encuentra un objeto para generar el formato de compresión especificado.</td>
<td>Ninguno</td>
<td>No aplicable</td>
</tr>
</tbody>
</table>



 

Los siguientes errores nunca deben producirse. Si encuentra uno de estos errores, envíe un informe de errores a Microsoft.



| Código de error                 | Descripción                                 |
|----------------------------|---------------------------------------------|
| ANÁLISIS DE ESCALA \_ DE TIEMPO DE DEX IDS \_ \_  | Error inesperado al analizar la escala de tiempo.      |
| ERROR DE DEX \_ IDS \_ GRAPH \_     | Error inesperado al compilar el gráfico de filtro. |
| ERROR DE LA \_ CUADRÍCULA DE DEX IDS \_ \_      | Error inesperado con la cuadrícula interna.    |
| ERROR DE LA \_ INTERFAZ DE DEX IDS \_ \_ | Error inesperado al obtener una interfaz.      |



 

 

 




