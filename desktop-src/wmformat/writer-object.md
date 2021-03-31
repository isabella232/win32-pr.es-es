---
title: Objeto de Writer
description: Objeto de Writer
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- SDK de Windows Media Format, objetos de escritor
- Advanced Systems Format (ASF), objetos Writer
- ASF (formato de sistemas avanzados), objetos de escritor
- objetos, objetos de escritura
- objetos de escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789238"
---
# <a name="writer-object"></a>Objeto de Writer

El objeto de escritor se utiliza para escribir archivos multimedia digitales mediante la estructura de archivos de Advanced Systems Format (ASF). El proceso de escritura de un archivo multimedia digital implica muchos pasos internos del escritor, que coordina la compresión, la packetización y la multiplexación.

El objeto escritor incluye interfaces para la salida a archivos o una red, admite una interfaz de devolución de llamada y puede crear uno o más objetos de propiedades de medios de entrada.

La función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)crea el objeto de escritor, que establece un puntero a una interfaz **IWMWriter** . Las demás interfaces del objeto de escritor se pueden obtener llamando al método **QueryInterface** .

El objeto de escritor admite las siguientes interfaces.



| Interfaz                                          | Descripción                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Proporciona métodos para generar claves [*DRM*](wmformat-glossary.md) .                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | Configura el objeto de escritor para escribir un archivo que contiene una secuencia precifrada que se ajusta al protocolo Windows Media DRM 10 para dispositivos de red.                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Administra la especificación y recuperación de la información de encabezado, como metadatos, [*marcadores*](wmformat-glossary.md), etc.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Administra la enumeración a través de la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Administra la enumeración a través de la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**.                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Proporciona acceso a información sobre los sistemas de marcas de agua presentes en el sistema.                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Inicia y detiene la escritura de archivos ASF; incluye métodos para asignar búferes, establecer y recuperar propiedades de entrada, establecer perfiles y nombres de archivos de salida y desbloquear el escritor.         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Agrega, obtiene y quita objetos de receptor especificados; Recupera estadísticas, el número de receptores y el tiempo de reloj en el que está trabajando el escritor; y realiza otras funciones avanzadas.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Proporciona cierta funcionalidad avanzada, especialmente para controlar el vídeo desentrelazado. Hereda todos los métodos de **IWMWriterAdvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Proporciona funcionalidad adicional de escritura, incluida la capacidad de obtener estadísticas detalladas del escritor. Hereda todos los métodos de **IWMWriterAdvanced** y **IWMWriterAdvanced2**.                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Administra cierta funcionalidad de escritura avanzada relacionada con los ejemplos de postview. La vista previa está viendo la salida, normalmente desde un codificador, para comprobar que el proceso de codificación y descodificación funciona correctamente. |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Administra las fases de preprocesamiento realizadas por el escritor. Los pasos de preprocesamiento se usan para mejorar la calidad de la salida codificada.                                                                                  |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de la vista previa.



| Interfaz                                                      | Descripción                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Administra el modo en que se reciben los ejemplos sin comprimir del objeto escritor para obtener una vista previa de lo que está haciendo el códec. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




