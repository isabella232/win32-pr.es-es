---
title: Grabación de listas de reproducción que contienen archivos seguros
description: Grabación de listas de reproducción que contienen archivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- SDK de Windows Media Format, grabar listas de reproducción con archivos seguros
- SDK de Windows Media Format, listas de reproducción con archivos seguros
- Advanced Systems Format (ASF), grabar listas de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), grabación de listas de reproducción con archivos seguros
- Advanced Systems Format (ASF), listas de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), listas de reproducción con archivos seguros
- Administración de derechos digitales (DRM), grabar listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), grabar listas de reproducción con archivos seguros
- Administración de derechos digitales (DRM), listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), listas de reproducción con archivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105714345"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Grabación de listas de reproducción que contienen archivos seguros

Las licencias creadas con los objetos del SDK de Windows Media Rights Manager 10 pueden especificar el derecho para copiar un archivo en un disco compacto como parte de una lista de reproducción. Esta característica, denominada grabación de listas de reproducción, requiere que compruebe las licencias de todos los archivos de la lista de reproducción antes de empezar a copiar los datos. El SDK de Windows Media Format proporciona la interfaz [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) para realizar la comprobación de archivos.

Para implementar la grabación de listas de reproducción, realice los pasos siguientes:

1.  Cree una instancia del objeto lector o el objeto lector sincrónico. Para obtener más información, consulte [leer archivos ASF](reading-asf-files.md).
2.  Llame al método **QueryInterface** de la interfaz del lector ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obtener un puntero a la interfaz [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .
3.  Copie los nombres de archivo de la lista de reproducción en una matriz de cadenas de caracteres anchos. Los nombres de archivo de la matriz deben estar en el mismo orden en que aparecen en la lista de reproducción.
4.  Llame al método [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , pasando un puntero a la matriz creada en el paso 3, para inicializar la comprobación de la licencia para los archivos.
5.  Cuando se completa la comprobación de la licencia, el objeto de lector envía un \_ \_ \_ mensaje de grabación de la lista de reproducción WMT init a la implementación del método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Cuando la devolución de llamada reciba este mensaje, llame al método [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obtener los resultados de la comprobación de licencia. Este método toma una matriz de variables **HRESULT** que corresponden a los nombres de archivo de la matriz que se pasa a **InitPlaylistBurn**. Si todos los valores de la matriz de resultados son iguales a S \_ correcto, puede continuar. Si algún resultado es un código de error, no se debe copiar la lista de reproducción.
6.  Con la misma instancia del lector, abra y Lea cada archivo. Debe abrir los archivos en el orden en que aparecen los nombres de archivo en la matriz de nombres de archivo que se pasó a **InitPlaylistBurn**.
7.  Una vez copiados todos los archivos de la lista de reproducción, llame a [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) para completar el proceso de grabación de la lista de reproducción y liberar los recursos utilizados por el lector.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




