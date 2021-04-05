---
title: Descargar contenido multimedia
description: Descargar contenido multimedia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player tiendas en línea, descargar contenido multimedia
- tiendas en línea, descargar contenido multimedia
- tipo 1 tiendas en línea, descarga de contenido multimedia
- Windows Media Player tiendas en línea, descarga de contenido multimedia
- tiendas en línea, descarga de contenido multimedia
- tipo 1 almacenes en línea, descarga de contenido multimedia
- contenido multimedia, descargar
- descargar contenido multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420439"
---
# <a name="downloading-media-content"></a>Descargar contenido multimedia

Windows Media Player controla las descargas de archivos de música de la tienda en línea. Se puede iniciar una descarga cuando la página de detección llama a [external. download](external-download.md) o cuando el usuario elige, en el reproductor, descargar un conjunto de pistas. En cualquier caso, Windows Media Player llama a [IWMPContentPartner::D scargar](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), pasando una lista de contenedores de contenido que describe el conjunto de pistas que se van a descargar y una cookie que representa la transacción de descarga. El complemento de asociado de contenido debe llamar a [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una vez por cada pista del conjunto. Cuando el complemento llama a **DownloadTrack**, pasa un **valor HRESULT** en el parámetro *hrDownload* . Si el complemento pasa un código de operación correcta en *hrDownload*, Windows Media Player descarga la pista. Si el complemento pasa un código de error en *hrDownload*, el reproductor no descarga la pista. Para cada llamada que se va a **Descargar**, el complemento debe proporcionar la cookie de la transacción y el identificador de la pista en cuestión. En el caso de las pistas que se descargarán realmente, el complemento también debe proporcionar la dirección URL de la pista.

Una vez descargado un archivo, Windows Media Player actualiza automáticamente la biblioteca para reflejar la música recién adquirida. El reproductor proporciona información de estado al complemento acerca de la operación de descarga mediante una llamada a [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). En este método, el reproductor proporciona un **valor HRESULT** para indicar si la descarga se ha realizado correctamente o no, el identificador de la pista y la cadena de parámetros personalizados que la tienda en línea proporcionó al llamar a **DownloadTrack**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




