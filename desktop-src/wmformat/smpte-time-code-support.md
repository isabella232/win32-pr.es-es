---
title: Compatibilidad con código de tiempo de SMPTE
description: Compatibilidad con código de tiempo de SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows SDK de formato multimedia, códigos de tiempo SMPTE
- Formato de sistemas avanzados (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- Windows SDK de formato multimedia, interfaz IWMReaderTimecode
- Advanced Systems Format (ASF),IWMReaderTimecode (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTimecode
- Códigos de tiempo SMPTE, acerca de
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19e3d7a85c797a3b0247bedb2359b4b40b60e8d4f243f14e2c94175bb1e2740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929621"
---
# <a name="smpte-time-code-support"></a>Compatibilidad con código de tiempo de SMPTE

El SDK Windows Media Format proporciona compatibilidad limitada con el código de hora SMPTE, que es un formato de código de hora estándar para películas y televisión. Puede incluir datos de código de tiempo de SMPTE con ejemplos como extensiones de unidad de datos. La parte de datos de la extensión es una estructura DE DATOS DE EXTENSIÓN DE CÓDIGO DE TIEMPO [**DE WMT \_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) que contiene la información de la marca de tiempo SMPTE original.

El mantenimiento del código de tiempo de SMPTE en los archivos de ASF incluye límites de rendimiento. Cada ejemplo con una marca de tiempo de SMPTE asociada requiere el transporte de los 14 bytes de la estructura de marca de tiempo. En un escenario de streaming, este requisito de mayor ancho de banda podría ser catastrófico. Como resultado, se sugiere que los códigos de tiempo SMPTE solo se conserven en archivos ASF durante el proceso de edición de vídeo, que normalmente se realiza con archivos locales. Cuando se crea el archivo final, debe quitar las extensiones de unidad de datos.

Puede leer las marcas de tiempo de SMPTE igual que leería cualquier otra extensión de unidad de datos, pero los objetos de lectura proporcionan compatibilidad integrada para la búsqueda por código de tiempo de SMPTE. Para poder buscar marcas de tiempo de SMPTE, primero debe indexar el archivo por código de tiempo de SMPTE. Puede configurar el indexador para indexar códigos de tiempo mediante el [**método IWMIndexer2::Configure.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)

Con el lector asincrónico, puede navegar por un archivo mediante marcas de tiempo de SMPTE mediante los métodos de la interfaz [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) y el método [**IWMReaderAdvanced3::StartAtPosition.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) Con el lector sincrónico, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




