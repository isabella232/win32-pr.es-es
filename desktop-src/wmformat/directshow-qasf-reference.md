---
title: Referencia de QASF de DirectShow
description: Referencia de QASF de DirectShow
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- SDK de Windows Media Format, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, referencia de QASF
- Filtros de QASF, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421033"
---
# <a name="directshow-qasf-reference"></a>Referencia de QASF de DirectShow

Esta sección contiene referencias de programación para los siguientes filtros, interfaces y enumeraciones de QASF de DirectShow. La documentación del SDK de DirectShow contiene materiales de referencia y de programación para interfaces genéricas adicionales expuestas por estos filtros, como **IBaseFilter** y **IPin**, y para versiones anteriores de los componentes de qasf.

Para obtener una explicación del nombre de QASF, consulte [acerca de DirectShow](about-directshow.md).

Los siguientes filtros se incluyen con los componentes de QASF de DirectShow.



| Filter                                           | Descripción                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [Filtro de lector ASF de WM](wm-asf-reader-filter.md) | Lee y analiza archivos ASF locales o remotos.                      |
| [Filtro de escritor ASF de WM](wm-asf-writer-filter.md) | Crea archivos ASF a partir de flujos de entrada comprimidos o sin comprimir. |



 

Las siguientes interfaces se definen para su uso con los componentes de QASF de DirectShow.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Proporciona un método que permite que las aplicaciones se registren para las devoluciones de llamada desde los pines de entrada del [escritor ASF de WM](wm-asf-writer-filter.md) o los clavijas de salida del filtro de [lector ASF de WM](wm-asf-reader-filter.md) . Se usa en la indización y al agregar extensiones de unidad de datos. |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Implementado por aplicaciones y llamado por los filtros. Las aplicaciones usan el método One en esta interfaz para obtener información sobre los ejemplos individuales de la secuencia. Se usa en la indización y al agregar extensiones de unidad de datos.                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Implementado en el escritor ASF de WM. Lo usan las aplicaciones para especificar los perfiles y los parámetros de indización para el archivo.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Proporciona funciones de configuración adicionales en el escritor ASF de WM.                                                                                                                                                                                                             |



 

La enumeración, la estructura y los eventos siguientes se definen para su uso con los componentes de QASF de DirectShow.



| Enumeración                                                               | Descripción                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_\_parámetro ASFWRITERCONFIG \_ AM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Define los parámetros de configuración de filtro utilizados en los métodos [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) y [**SetParam**](iconfigasfwriter2-setparam.md) . |



 



| Estructura                                         | Descripción                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_datos de \_ evento \_ WMT de AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Contiene información relativa a un evento [**de \_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) y el código de estado asociado devuelto por el SDK de Windows Media Format. |



 



| Evento                                           | Descripción                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [\_evento WMT de EC \_](ec-wmt-event.md)              | Evento reenviado desde el SDK de Windows Media Format.                                                              |
| [\_evento de \_ Índice \_ WMT de EC](ec-wmt-index-event.md) | Se envía cuando una aplicación utiliza el [escritor ASF de WM](wm-asf-writer-filter.md) para indizar Windows Media Video archivos. |



 

 

 