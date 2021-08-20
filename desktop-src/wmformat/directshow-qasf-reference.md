---
title: DirectShow Referencia de QASF
description: DirectShow Referencia de QASF
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows SDK de formato multimedia, QASF
- Windows SDK de formato multimedia, DirectShow
- DirectShow,referencia de QASF
- Filtros QASF, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69029c02945f181ba8faa631c3320f461ddbf650ed337cdf895ee5204a57de21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655666"
---
# <a name="directshow-qasf-reference"></a>DirectShow Referencia de QASF

Esta sección contiene referencias de programación para las siguientes DirectShow filtros, interfaces y enumeraciones de QASF. La documentación del SDK de DirectShow contiene materiales de referencia y guía de programación para interfaces genéricas adicionales expuestas por estos filtros, como **IBaseFilter** e **IPin,** y para versiones anteriores de los componentes qasF.

Para obtener una explicación del nombre de QASF, vea [Acerca de DirectShow](about-directshow.md).

Los siguientes filtros se incluyen con los componentes DirectShow QASF.



| Filter                                           | Descripción                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [Filtro de lector de ASF de WM](wm-asf-reader-filter.md) | Lee y analiza archivos ASF locales o remotos.                      |
| [Filtro de escritor de ASF de WM](wm-asf-writer-filter.md) | Crea archivos ASF a partir de flujos de entrada comprimidos o sin comprimir. |



 

Las interfaces siguientes se definen para su uso con los DirectShow QASF.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Proporciona un método que permite que las aplicaciones se registren para las devoluciones de llamada de los pins de entrada del escritor [de ASF](wm-asf-writer-filter.md) de WM o de los pines de salida del filtro [lector de ASF de WM.](wm-asf-reader-filter.md) Se usa en la indexación y al agregar extensiones de unidad de datos. |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Implementado por aplicaciones y llamado por los filtros. Las aplicaciones usan el único método de esta interfaz para obtener información sobre muestras individuales en la secuencia. Se usa en la indexación y al agregar extensiones de unidad de datos.                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Se implementa en WM ASF Writer. Lo usan las aplicaciones para especificar perfiles y parámetros de indexación para el archivo.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Proporciona funciones de configuración adicionales en WM ASF Writer.                                                                                                                                                                                                             |



 

La enumeración, la estructura y los eventos siguientes se definen para su uso con los DirectShow QASF.



| Enumeración                                                               | Descripción                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Define los parámetros de configuración de filtro usados en los [**métodos IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) [**y SetParam.**](iconfigasfwriter2-setparam.md) |



 



| Estructura                                         | Descripción                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS \_ DE EVENTOS DE AM WMT \_ \_**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Contiene información relacionada con un evento [**WMT \_ STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) y el código de estado asociado devuelto por el SDK Windows Media Format. |



 



| Evento                                           | Descripción                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [EVENTO \_ WMT \_ DE EC](ec-wmt-event.md)              | Evento reenviado desde Windows SDK de formato multimedia.                                                              |
| [EVENTO \_ DE ÍNDICE WMT DE \_ \_ EC](ec-wmt-index-event.md) | Se envía cuando una aplicación usa [WM ASF Writer para](wm-asf-writer-filter.md) indexar Windows archivos de vídeo multimedia. |



 

 

 