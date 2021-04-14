---
title: Compatibilidad con código de tiempo SMPTE
description: Compatibilidad con código de tiempo SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- SDK de Windows Media Format, códigos de tiempo SMPTE
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- SDK de Windows Media Format, interfaz IWMReaderTimecode
- Advanced Systems Format (ASF), IWMReaderTimecode (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTimecode
- Códigos de tiempo SMPTE, acerca de
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532992"
---
# <a name="smpte-time-code-support"></a>Compatibilidad con código de tiempo SMPTE

El SDK de Windows Media Format proporciona compatibilidad limitada para el código de tiempo SMPTE, que es un formato de código de hora estándar para películas y televisión. Puede incluir datos de código de tiempo SMPTE con ejemplos como extensiones de unidad de datos. La parte de datos de la extensión es una estructura de [**\_ datos de extensión de código de tiempo \_ \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que contiene la información de la marca de tiempo de SMPTE original.

El mantenimiento del código de tiempo SMPTE en los archivos ASF incluye límites de rendimiento. Cada ejemplo con una marca de tiempo de SMPTE asociada requiere el transporte de los 14 bytes en la estructura de la marca de tiempo. En un escenario de streaming, este mayor requisito de ancho de banda podría ser catastrófico. Como resultado, se recomienda que los códigos de tiempo de SMPTE solo se almacenen en archivos ASF durante el proceso de edición de vídeo, que normalmente se realiza con archivos locales. Cuando se cree el archivo final, debe quitar las extensiones de unidad de datos.

Puede leer las marcas de tiempo de SMPTE tal como lo haría con cualquier otra extensión de unidad de datos, pero los objetos de lectura proporcionan compatibilidad integrada para la búsqueda por código de tiempo de SMPTE. Para poder buscar marcas de tiempo de SMPTE, primero debe indexar el archivo por código de tiempo de SMPTE. Puede configurar el indexador para indexar los códigos de tiempo mediante el método [**IWMIndexer2:: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .

Con el lector asincrónico, puede navegar por las marcas de tiempo de SMPTE en un archivo mediante los métodos de la interfaz [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) y el método [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) . Con el lector sincrónico, use [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




