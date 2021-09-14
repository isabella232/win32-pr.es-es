---
description: Errores de representación
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errores de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362331"
---
# <a name="rendering-errors"></a>Errores de representación

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) define varios códigos de error que se usan para registrar errores de representación. Si un proyecto no se representa correctamente, el motor de representación llama al [**método IAMErrorLog::LogError.**](iamerrorlog-logerror.md) En la tabla siguiente se resumen los parámetros dados a **LogError**:

-   El código de error está incluido en el *parámetro ErrorCode.*
-   La descripción está contenida en el parámetro ErrorString.
-   La descripción está contenida en el *parámetro ErrorString.*
-   Si hay información adicional, el tipo **VARIANT** se encuentra en el miembro **vt** de **variant** al que apunta *pExtraInfo.*

> [!Note]  
> Los códigos de error que se describen aquí no son **valores HRESULT.** Para obtener una lista de **valores devueltos HRESULT** específicos de DES, vea [Códigos de error y de éxito.](error-and-success-codes.md)

 




| Código de error | Descripción | Información adicional | Tipo Variant | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | El nombre de archivo no existe o DirectShow no reconoce la extensión de archivo. | Nombre de archivo | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | El tipo de archivo no coincide con la extensión de archivo o el archivo está dañado. | Nombre de archivo | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | El nombre de archivo era necesario, pero no se ha especificado. | Ninguno | No aplicable | 
| DEX_IDS_UNKNOWN_SOURCE | No se puede analizar el origen de datos proporcionado por este origen. | Ninguno | No aplicable | 
| DEX_IDS_INSTALL_PROBLEM | error inesperado. Algunos DirectShow componente no están instalados correctamente. | Ninguno | No aplicable | 
| DEX_IDS_NO_SOURCE_NAMES | El filtro de origen no acepta nombres de archivo. | Ninguno | No aplicable | 
| DEX_IDS_BAD_MEDIATYPE | No se admite el tipo de medio del grupo. | Número de grupo | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | Número de secuencia no válido para este origen. | Número de secuencia | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | Memoria insuficiente | Ninguno | No aplicable | 
| DEX_IDS_DIBSEQ_NOTALLSAME | Un mapa de bits de la secuencia no era del mismo tipo que los demás. | Nombre del mapa de bits | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | Los tiempos de los medios del clip no son válidos o la secuencia de mapa de bits independiente del dispositivo (DIB) es demasiado corta.<blockquote>[!Note]<br />Si se producen otros errores de representación, este error puede producirse aunque los tiempos de los medios sean válidos.</blockquote><br /> | Ninguno | No aplicable | 
| DEX_IDS_INVALID_DXT | El identificador de clase (CLSID) del efecto o la transición no es válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | El CLSID del efecto o transición predeterminados no es válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | La versión de DirectX no admite transiciones tridimensionales. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | Este efecto no es el tipo correcto o se ha roto. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | No existe ninguna propiedad de este tipo en el objeto . | Nombre de propiedad | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | Valor no válido para esta propiedad. | Valor especificado | <strong>VARIANTE</strong> | 
| DEX_IDS_INVALID_XML | Error de sintaxis en el archivo XML. | Número de línea | VT_I4 (entero de 4 bytes) | 
| DEX_IDS_CANT_FIND_FILTER | No se encuentra el filtro especificado en XML por categoría e instancia. | Nombre descriptivo (instancia) | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | Error al escribir un archivo XML en el disco. | Ninguno | No aplicable | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID no es un filtro DirectShow efecto de audio válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | No se encuentra un objeto para generar el formato de compresión especificado. | Ninguno | No aplicable | 




 

Los siguientes errores nunca deben producirse. Si encuentra uno de estos errores, envíe un informe de errores a Microsoft.



| Código de error                 | Descripción                                 |
|----------------------------|---------------------------------------------|
| ANÁLISIS DE ESCALA \_ DE TIEMPO DE DEX IDS \_ \_  | Error inesperado al analizar la escala de tiempo.      |
| ERROR DEL \_ GRAFO DE DEX IDS \_ \_     | Error inesperado al compilar el gráfico de filtro. |
| ERROR DE DEX \_ IDS \_ GRID \_      | Error inesperado con la cuadrícula interna.    |
| ERROR DE LA \_ INTERFAZ DE DEX IDS \_ \_ | Error inesperado al obtener una interfaz.      |



 

 

 




