---
title: Indexer (objeto)
description: Indexer (objeto)
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- SDK de Windows Media Format, objetos de indexador
- Advanced Systems Format (ASF), objetos de indexador
- ASF (formato de sistemas avanzados), objetos de indexador
- objetos, objetos de indexador
- objetos de indexador
- índices, objetos de indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104077429"
---
# <a name="indexer-object"></a>Indexer (objeto)

El objeto indexador crea un índice en un archivo ASF. Un índice es una parte estándar de un archivo ASF que equipara las muestras de vídeo con las horas, los números de fotogramas o, si procede, la sociedad de las marcas de tiempo estándar de las imágenes de movimiento y los ingenieros de televisión (SMPTE). Sin un índice, ni el objeto lector ni el objeto lector sincrónico pueden buscar un punto en medio de un archivo.

Los índices creados por este objeto solo son necesarios si el archivo contiene una o varias secuencias de vídeo. Esto se debe a que los datos de audio no se comprimen temporalmente, lo que facilita la búsqueda de un tiempo determinado en una secuencia de audio.

El objeto de indexador se crea mediante la función [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , que establece un puntero a una interfaz **IWMIndexer** . Las demás interfaces del objeto indexador se pueden obtener llamando al método **QueryInterface** .

El objeto de indexador admite las siguientes interfaces.



| Interfaz                          | Descripción                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Inicia y detiene el proceso de indización.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configura el indexador, habilitando la indexación por fotograma, por hora o por código de tiempo de SMPTE. |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de indexador.



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




