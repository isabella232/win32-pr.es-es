---
title: Objeto receptor de archivos de Writer
description: Objeto receptor de archivos de Writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- SDK de Windows Media Format, objetos de receptor de archivos de escritura
- Advanced Systems Format (ASF), objetos de receptor de archivos de escritor
- ASF (formato de sistemas avanzados), objetos de receptor de archivos de escritor
- objetos, objetos de receptor de archivos de escritor
- objetos de receptor de archivo de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077450"
---
# <a name="writer-file-sink-object"></a>Objeto receptor de archivos de Writer

El objeto de receptor del archivo de escritura se utiliza al escribir la salida de Windows Media en un archivo.

La función [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)crea el objeto de receptor del archivo de escritura, que establece un puntero a una interfaz **IWMWriterFileSink** . Las demás interfaces del objeto de receptor del archivo de escritor se pueden obtener llamando al método **QueryInterface** .

El objeto de receptor del archivo de escritor admite las siguientes interfaces.



| Interfaz                                          | Descripción                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que la aplicación obtenga mensajes de estado del objeto.                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Abre un archivo en el que el objeto de escritura puede escribir datos.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Proporciona administración extendida de un objeto de receptor de archivos. Hereda todos los métodos de **IWMWriterFileSink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Proporciona opciones adicionales para escribir archivos. Hereda todos los métodos de **IWMWriterFileSink** y **IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Asigna memoria, determina si el receptor está funcionando en tiempo real y controla varias funciones de devolución de llamada.                |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor del archivo de escritura.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatorio cuando la información de estado se debe comunicar a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




