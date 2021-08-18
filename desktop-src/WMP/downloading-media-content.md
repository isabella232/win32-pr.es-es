---
title: Descargar contenido multimedia
description: Descargar contenido multimedia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Reproductor de Windows Media en línea, descargar contenido multimedia
- tiendas en línea, descarga de contenido multimedia
- tiendas en línea de tipo 1, descarga de contenido multimedia
- Reproductor de Windows Media en línea, descarga de contenido multimedia
- tiendas en línea, descarga de contenido multimedia
- tiendas en línea de tipo 1, descarga de contenido multimedia
- contenido multimedia, descarga
- descargar contenido multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997040"
---
# <a name="downloading-media-content"></a>Descargar contenido multimedia

Reproductor de Windows Media las descargas de archivos de música para la tienda en línea. Se puede iniciar una descarga cuando la página de detección llama a [External.download](external-download.md) o cuando el usuario elige, en el Reproductor, descargar un conjunto de pistas. En cualquier caso, Reproductor de Windows Media llama a [IWMPContentPartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), pasando una lista de contenedores de contenido que describe el conjunto de pistas que se descargarán y una cookie que representa la transacción de descarga. A continuación, el complemento del asociado de contenido debe llamar a [IWMPContentPartnerCallback::D ownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una vez para cada pista del conjunto. Cuando el complemento llama a **DownloadTrack,** pasa un **HRESULT** en el *parámetro hrDownload.* Si el complemento pasa un código correcto en *hrDownload,* Reproductor de Windows Media descarga la pista. Si el complemento pasa un código de error en *hrDownload*, el reproductor no descarga la pista. Para cada llamada a **Descargar**, el complemento debe proporcionar la cookie de transacción y el identificador de la pista en cuestión. Para las pistas que se descargarán realmente, el complemento también debe proporcionar la dirección URL de la pista.

Una vez descargado un archivo, Reproductor de Windows Media actualiza automáticamente la biblioteca para reflejar la música recién comprada. El reproductor proporciona información de estado al complemento sobre la operación de descarga mediante una llamada a [IWMPContentPartner::D ownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). En este método, el reproductor proporciona un **HRESULT** para indicar que la descarga se ha descargado correctamente o no, el identificador de pista y la cadena de parámetros personalizados que la tienda en línea proporcionó cuando llamó **a DownloadTrack**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




