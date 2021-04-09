---
title: Colecciones de fuentes personalizadas (Windows 7/8)
description: DirectWrite proporciona acceso a la colección de fuentes del sistema mediante el método IDWriteFactory GetSystemFontCollection.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792663"
---
# <a name="custom-font-collections-windows-78"></a>Colecciones de fuentes personalizadas (Windows 7/8)

[DirectWrite](direct-write-portal.md) proporciona acceso a la colección de fuentes del sistema mediante el método [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Esta es la colección de fuentes que se usa con más frecuencia. Sin embargo, algunas aplicaciones tienen que usar fuentes que no están instaladas en el sistema, como los archivos de fuente incluidos o los archivos de fuentes incrustados en la aplicación.

Si las fuentes que desea no están en la colección de fuentes del sistema, puede crear una colección de fuentes personalizada derivada de [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Esta información general consta de las siguientes partes:

-   [Registrar y anular el registro de un cargador de colecciones de fuentes](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrar y anular el registro de un cargador de colecciones de fuentes

Registre un cargador de colección de fuentes mediante el método [**IDWriteFactory:: RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) y pasándole una interfaz [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada por la aplicación como un objeto singleton. Este objeto cargará las fuentes cuando se solicite la colección personalizada. Tanto la colección de fuentes del sistema como las colecciones de fuentes personalizadas se almacenan en caché, por lo que las fuentes solo se cargan una vez.

El cargador de la colección de fuentes se debe descargar finalmente mediante [**IDWriteFactory:: UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> El registro del cargador de la colección de fuentes se agrega al recuento de referencias; no llame a [**UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) desde dentro del destructor o el objeto del cargador de la colección nunca se eliminará del registro.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Cree un objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) mediante [**IDWriteFactory:: CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) y pasándole una clave definida por la aplicación. La clave es un puntero void y el tipo de datos, el formato y el significado están definidos por la aplicación y son opacos para el sistema de fuentes.

Mientras que la clave puede ser cualquier cosa, [DirectWrite](direct-write-portal.md) requiere que cada clave sea:

-   Es único para una colección de fuentes única dentro del ámbito del cargador.
-   Válido hasta que se anule el registro del cargador mediante el generador.

Cuando se llama al método [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) , [DirectWrite](direct-write-portal.md) vuelve a llamar a una interfaz [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada como un objeto singleton por parte de la aplicación. DirectWrite usa el método de devolución de llamada [**IDWriteFontCollectionLoader:: CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) para recuperar un objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implementado por la aplicación. El objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) que se usa para crear la colección se pasa a este método y debe ser utilizado por el enumerador de archivos de fuente para crear los objetos [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) que se van a incluir en la colección.

La clave pasada a este método identifica la colección de fuentes y es la misma clave que se pasa a [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection).

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

El objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) definido por la aplicación creado por el método [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) se utiliza para enumerar los archivos de fuente de una colección, creando un objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) para cada archivo. El método [**IDWriteFontFileEnumerator:: MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) cambia la posición al siguiente archivo de fuente. Si hay un archivo en la posición, se establecerá el valor de *hasCurrentFile* en **true**. De lo contrario, se establecerá en **false** y el método devolverá los valores **\_ correctos**.

> [!Note]  
> El enumerador de archivo de fuente debe comenzar a colocarse antes del primer elemento y avanzado en la primera llamada a [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext).

 

El método [**IDWriteFontFileEnumerator:: GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) genera un objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) . Si no hay ningún archivo de fuentes en la posición actual, ya que no se ha llamado a [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) o hasCurrentFile se ha establecido en **false**, **GetCurrentFontFile** devolverá **E \_ producirá un error**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

La salida del objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) de [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) se puede crear llamando a [**IDWriteFactory:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). La clave de referencia de archivo de fuente identifica una referencia de archivo de fuente específica y debe ser única en el cargador de archivos de fuentes que cargará el archivo.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

El método [**CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) toma un objeto [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementado por la aplicación que se usa para cargar la fuente. El método de devolución de llamada [**IDWriteFontFileLoader:: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) pasa la clave y genera un objeto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) .

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

El objeto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implementado por la aplicación proporciona los datos de archivo de fuente para una referencia de archivo de fuente de un cargador de archivos de fuentes personalizado. Junto con el tamaño de archivo y la hora de la última escritura, proporciona un método ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) para recuperar los fragmentos de archivo que se van a compilar en un objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) .

> [!Note]  
> Las implementaciones de [**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) deben devolver un error si el fragmento solicitado está fuera de los límites del archivo.

 

Un [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) puede obtener el contenido del archivo de fuente desde cualquier lugar, como la unidad de disco duro local o los recursos incrustados.

 

 