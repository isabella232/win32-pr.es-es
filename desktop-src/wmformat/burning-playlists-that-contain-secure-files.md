---
title: Grabación de listas de reproducción que contienen archivos seguros
description: Grabación de listas de reproducción que contienen archivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows SDK de formato multimedia, listas de reproducción de reproducción con archivos seguros
- Windows SDK de formato multimedia, listas de reproducción con archivos seguros
- Formato de sistemas avanzados (ASF), listas de reproducción de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), listas de reproducción de reproducción con archivos seguros
- Formato de sistemas avanzados (ASF), listas de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), listas de reproducción con archivos seguros
- administración de derechos digitales (DRM), reproducción de listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), reproducción de listas de reproducción con archivos seguros
- administración de derechos digitales (DRM), listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), listas de reproducción con archivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570249"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Grabación de listas de reproducción que contienen archivos seguros

Las licencias creadas mediante los objetos del SDK de Windows Media Rights Manager 10 pueden especificar el derecho de copiar un archivo en un disco compacto como parte de una lista de reproducción. Esta característica, denominada grabación de listas de reproducción, requiere que compruebe las licencias de todos los archivos de la lista de reproducción antes de empezar a copiar los datos. El SDK Windows Media Format proporciona la [**interfaz IWMReaderPlaylistReader Para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) realizar la comprobación de archivos automáticamente.

Para implementar la reproducción de listas de reproducción, realice los pasos siguientes:

1.  Cree una instancia del objeto de lector o del objeto de lector sincrónico. Para obtener más información, vea [Lectura de archivos ASF.](reading-asf-files.md)
2.  Llame al **método QueryInterface** de la interfaz del lector ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obtener un puntero a la [**interfaz IWMReaderPlaylistInterface.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn)
3.  Copie los nombres de archivo de la lista de reproducción en una matriz de cadenas de caracteres anchos. Los nombres de archivo de la matriz deben estar en el mismo orden que aparecen en la lista de reproducción.
4.  Llame al [**método IWMReaderPlaylistAsync::InitPlaylistAsync**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) y pase un puntero a la matriz creada en el paso 3 para inicializar la comprobación de la licencia de los archivos.
5.  Cuando se completa la comprobación de la licencia, el objeto reader envía un mensaje WMT INIT PLAYLIST BURN a la implementación del método de devolución de llamada \_ \_ \_ [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Cuando la devolución de llamada reciba este mensaje, llame al método [**IWMReaderPlaylistAsync::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obtener los resultados de la comprobación de licencia. Este método toma una matriz de variables **HRESULT** que se corresponden con los nombres de archivo de la matriz pasada a **InitPlaylistAsync**. Si todos los valores de la matriz de resultados son iguales a S \_ OK, puede continuar. Si algún resultado es un código de error, no se debe copiar la lista de reproducción.
6.  Con la misma instancia del lector, abra y lea cada archivo. Debe abrir los archivos en el orden en que aparecían los nombres de archivo en la matriz de nombres de archivo que se pasó a **InitPlaylistMatriz.**
7.  Cuando haya copiado todos los archivos de la lista de reproducción, llame a [**IWMReaderPlaylist Usb::EndPlaylistPlay Para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) completar el proceso de grabación de la lista de reproducción y liberar los recursos usados por el lector.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




