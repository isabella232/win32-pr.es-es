---
title: Objeto indexador
description: Objeto indexador
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows SDK de formato multimedia, objetos de indexador
- Formato de sistemas avanzados (ASF), objetos de indexador
- ASF (formato de sistemas avanzados), objetos de indexador
- objects,indexer objects
- objetos de indexador
- indexes,indexer objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795ef166f6b3ad46897305cbd3f6c38bbc7a219bb99df1dcf8b14dbfb1443577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839792"
---
# <a name="indexer-object"></a>Objeto indexador

El objeto indexador crea un índice en un archivo ASF. Un índice es una parte estándar de un archivo ASF que equivale a las muestras de vídeo con tiempos, números de fotograma o (si procede) marcas de tiempo estándar de la Sociedad de Ingenieros de Imagen de Movimiento e Televisión (SMPTE). Sin un índice, ni el objeto lector ni el objeto de lector sincrónico pueden buscar un punto en medio de un archivo.

Los índices creados por este objeto solo son necesarios si el archivo contiene una o varias secuencias de vídeo. Esto se debe a que los datos de audio no se comprimen temporalmente, lo que facilita la tarea de encontrar una hora determinada en una secuencia de audio.

La función [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) crea el objeto indexador, que establece un puntero a una **interfaz IWMIndexer.** Las demás interfaces del objeto indexador se pueden obtener llamando al **método QueryInterface.**

El objeto indexador admite las interfaces siguientes.



| Interfaz                          | Descripción                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Inicia y detiene el proceso de indexación.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configura el indexador, habilitando la indexación por fotograma, por tiempo o por código de tiempo de SMPTE. |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de indexador.



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




