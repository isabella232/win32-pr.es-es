---
title: Objeto de Writer
description: Objeto de Writer
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows SDK de formato multimedia, objetos de escritor
- Formato de sistemas avanzados (ASF), objetos de escritura
- ASF (formato de sistemas avanzados), objetos de escritura
- objects,writer objects
- objetos writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f76ad82cb56317cef9b70b0412fb79662ef89eacace8668b08a06f4cc5bf420
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119392325"
---
# <a name="writer-object"></a>Objeto de Writer

El objeto de escritor se usa para escribir archivos multimedia digitales mediante la estructura de archivos de formato de sistemas avanzados (ASF). El proceso de escritura de un archivo multimedia digital implica muchos pasos internos para el escritor, que coordina la compresión, la creación de paquetes y la multiplexación.

El objeto de escritor incluye interfaces para la salida a archivos o una red, admite una interfaz de devolución de llamada y puede crear uno o varios objetos de propiedades multimedia de entrada.

La función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)crea el objeto writer , que establece un puntero a una **interfaz IWMWriter.** Las demás interfaces del objeto de escritor se pueden obtener llamando al **método QueryInterface.**

El objeto de escritor admite las interfaces siguientes.



| Interfaz                                          | Descripción                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Proporciona métodos para generar [*claves DRM.*](wmformat-glossary.md)                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | Configura el objeto de escritor para escribir un archivo que contiene una secuencia pre cifrada que se ajusta al protocolo DRM 10 de multimedia para dispositivos de red de Windows.                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Administra la especificación y recuperación de información de encabezado, como [*metadatos, marcadores,*](wmformat-glossary.md)y así sucesivamente.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Administra la enumeración a través de la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Administra la enumeración a través de la información de códec disponible. Hereda todos los métodos de **IWMHeaderInfo** **e IWMHeaderInfo2.**                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Proporciona acceso a información sobre los sistemas de marca de agua presentes en el sistema.                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Inicia y detiene la escritura de archivos ASF; incluye métodos para asignar búferes, establecer y recuperar propiedades de entrada, establecer perfiles y nombres de archivo de salida y desbloquear el escritor.         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Agrega, obtiene y quita los objetos receptores especificados; recupera las estadísticas, el número de receptores y la hora del reloj en la que está trabajando el escritor. y realiza otras funciones avanzadas.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Proporciona algunas funcionalidades avanzadas, especialmente para controlar vídeo desenlazado. Hereda todos los métodos de **IWMWriterAdvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Proporciona funcionalidad de escritor adicional, incluida la capacidad de obtener estadísticas detalladas del escritor. Hereda todos los métodos de **IWMWriterAdvanced** **e IWMWriterAdvanced2**.                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Administra algunas funcionalidades avanzadas de escritura relacionadas con ejemplos de vistas posteriores. La vista posterior está viendo la salida, normalmente desde un codificador, para comprobar que el proceso de codificación/decodización funciona correctamente. |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Administra los pases de preprocesamiento realizados por el escritor. Los pases de preprocesamiento se usan para mejorar la calidad de la salida codificada.                                                                                  |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar un seguimiento del progreso de la vista posterior.



| Interfaz                                                      | Descripción                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Administra cómo se reciben muestras sin comprimir del objeto de escritor para obtener una vista previa de lo que hace el códec. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




