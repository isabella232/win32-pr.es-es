---
title: Objeto receptor de archivos de Writer
description: Objeto receptor de archivos de Writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows SDK de formato multimedia, objetos receptores de archivos de escritor
- Formato de sistemas avanzados (ASF), objetos receptores de archivos de escritura
- ASF (formato de sistemas avanzados), objetos receptores de archivos de escritura
- objects,writer file sink objects
- objetos receptores de archivos de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466201"
---
# <a name="writer-file-sink-object"></a>Objeto receptor de archivos de Writer

El objeto receptor del archivo de escritura se usa al escribir Windows salida multimedia en un archivo.

La función [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)crea el objeto receptor del archivo de escritura , que establece un puntero a una **interfaz IWMWriterFileSink.** Las demás interfaces del objeto receptor del archivo de escritura se pueden obtener llamando al **método QueryInterface.**

El objeto receptor del archivo de escritura admite las interfaces siguientes.



| Interfaz                                          | Descripción                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que la aplicación obtenga mensajes de estado del objeto .                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Abre un archivo en el que el objeto de escritor puede escribir datos.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Proporciona administración extendida de un objeto receptor de archivos. Hereda todos los métodos de **IWMWriterFileSink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Proporciona opciones adicionales para escribir archivos. Hereda todos los métodos de **IWMWriterFileSink** **e IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Asigna memoria, determina si el receptor funciona en tiempo real y controla varias funciones de devolución de llamada.                |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar un seguimiento del progreso de un objeto receptor de archivo de escritura.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Se requiere cuando la información de estado se debe comunicar a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




