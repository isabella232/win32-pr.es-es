---
title: Colecciones de fuentes personalizadas (Windows 7/8)
description: DirectWrite proporciona acceso a la colección de fuentes del sistema mediante el método IDWriteFactory GetSystemFontCollection.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc76214dda067b43c27c8e04e4419f147d0e33b7566b4dedc5ac3255a1c1dc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290765"
---
# <a name="custom-font-collections-windows-78"></a>Colecciones de fuentes personalizadas (Windows 7/8)

[DirectWrite](direct-write-portal.md) proporciona acceso a la colección de fuentes del sistema mediante el [**método IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Esta es la colección de fuentes que se usa con más frecuencia. Sin embargo, algunas aplicaciones tienen que usar fuentes que no están instaladas en el sistema, como los archivos de fuente incluidos o los archivos de fuente insertados en la aplicación.

Si las fuentes que desea no están en la colección de fuentes del sistema, puede crear una colección de fuentes personalizada derivada de [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Esta información general consta de las siguientes partes:

-   [Registro y anulación del registro de un cargador de colecciones de fuentes](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registro y anulación del registro de un cargador de colecciones de fuentes

Para registrar un cargador de colecciones de fuentes, use el método [**IDWriteFactory::RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) y pase una interfaz [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada por la aplicación como un objeto singleton. Este objeto cargará las fuentes cuando se solicite la colección personalizada. Tanto la colección de fuentes del sistema como las colecciones de fuentes personalizadas se almacenan en caché, por lo que las fuentes solo se cargan una vez.

El cargador de colecciones de fuentes se debe descargar finalmente mediante [**IDWriteFactory::UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> El registro del cargador de la colección de fuentes agrega al recuento de referencias; no llame a [**UnregisterFontCollectionLoader desde**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) el destructor o el objeto del cargador de recopilación nunca se anulará del registro.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Se crea un [**objeto IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) mediante [**IDWriteFactory::CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) y se le pasa una clave definida por la aplicación. La clave es un puntero void y la aplicación define el tipo de datos, el formato y el significado y son opacos para el sistema de fuentes.

Mientras que la clave puede ser cualquier cosa, [DirectWrite](direct-write-portal.md) requiere que cada clave sea:

-   Único para una colección de fuentes única dentro del ámbito del cargador.
-   Válido hasta que se anula el registro del cargador mediante el generador.

Cuando se llama al método [](direct-write-portal.md) [**CreateCustomFontCollection,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) DirectWrite a una interfaz [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada como un objeto singleton por la aplicación. El método de devolución de llamada [**IDWriteFontCollectionLoader::CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) lo usa DirectWrite para recuperar un objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implementado por la aplicación. El [**objeto IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) que se usa para crear la colección se pasa a este método y debe ser utilizado por el enumerador de archivos de fuente para crear los objetos [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) que se incluirán en la colección.

La clave pasada a este método identifica la colección de fuentes y es la misma clave pasada a [**CreateCustomFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

El objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) definido por la aplicación creado por el método [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) se usa para enumerar los archivos de fuente de una colección, creando un objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) para cada archivo. El [**método IDWriteFontFileEnumerator::MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) cambia la posición al siguiente archivo de fuente. Si hay un archivo en la posición, establecerá *hasCurrentFile* en **TRUE.** De lo contrario, se establecerá **en FALSE** y el método devolverá **S \_ OK**.

> [!Note]  
> El enumerador de archivos de fuente debe empezar situado delante del primer elemento y avanzar en la primera llamada a [**MoveNext.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)

 

El [**método IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) genera un objeto [**IDWriteFontFileEnumerator::GetCurrentFontFile.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) Si no hay ningún archivo de fuente en la posición actual, porque [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) aún no se ha llamado o hasCurrentFile se ha establecido en **FALSE,** **GetCurrentFontFile** devolverá **E \_ FAIL**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

La [**salida del objeto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) de [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) se puede crear llamando a [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). La clave de referencia del archivo de fuente identifica una referencia de archivo de fuente específica y debe ser única dentro del cargador de archivos de fuente que cargará el archivo.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

El [**método CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) toma un [**objeto IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementado por la aplicación que se usa para cargar la fuente. Al método de devolución de llamada [**IDWriteFontFileLoader::CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) se le pasa la clave y genera un [**objeto IDWriteFontFileStream.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

El objeto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implementado por la aplicación proporciona los datos del archivo de fuente para una referencia de archivo de fuente de un cargador de archivos de fuente personalizado. Junto con el tamaño del archivo y la hora de la última escritura, proporciona un método ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) para recuperar fragmentos de archivo que se van a compilar en un [**objeto IDWriteFontFile.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)

> [!Note]  
> [**Las implementaciones readFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) deben devolver un error si el fragmento solicitado está fuera de los límites de archivo.

 

[**IdWriteFontFileStream puede**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) obtener el contenido del archivo de fuente desde cualquier lugar, como la unidad de disco duro local o los recursos incrustados.

 

 