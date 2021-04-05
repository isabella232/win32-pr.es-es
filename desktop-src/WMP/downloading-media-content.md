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
# <a name="downloading-media-content"></a><span data-ttu-id="88edb-111">Descargar contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="88edb-111">Downloading Media Content</span></span>

<span data-ttu-id="88edb-112">Windows Media Player controla las descargas de archivos de música de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="88edb-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="88edb-113">Se puede iniciar una descarga cuando la página de detección llama a [external. download](external-download.md) o cuando el usuario elige, en el reproductor, descargar un conjunto de pistas.</span><span class="sxs-lookup"><span data-stu-id="88edb-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="88edb-114">En cualquier caso, Windows Media Player llama a [IWMPContentPartner::D scargar](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), pasando una lista de contenedores de contenido que describe el conjunto de pistas que se van a descargar y una cookie que representa la transacción de descarga.</span><span class="sxs-lookup"><span data-stu-id="88edb-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="88edb-115">El complemento de asociado de contenido debe llamar a [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una vez por cada pista del conjunto.</span><span class="sxs-lookup"><span data-stu-id="88edb-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="88edb-116">Cuando el complemento llama a **DownloadTrack**, pasa un **valor HRESULT** en el parámetro *hrDownload* .</span><span class="sxs-lookup"><span data-stu-id="88edb-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="88edb-117">Si el complemento pasa un código de operación correcta en *hrDownload*, Windows Media Player descarga la pista. Si el complemento pasa un código de error en *hrDownload*, el reproductor no descarga la pista. Para cada llamada que se va a **Descargar**, el complemento debe proporcionar la cookie de la transacción y el identificador de la pista en cuestión.</span><span class="sxs-lookup"><span data-stu-id="88edb-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="88edb-118">En el caso de las pistas que se descargarán realmente, el complemento también debe proporcionar la dirección URL de la pista.</span><span class="sxs-lookup"><span data-stu-id="88edb-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="88edb-119">Una vez descargado un archivo, Windows Media Player actualiza automáticamente la biblioteca para reflejar la música recién adquirida.</span><span class="sxs-lookup"><span data-stu-id="88edb-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="88edb-120">El reproductor proporciona información de estado al complemento acerca de la operación de descarga mediante una llamada a [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span><span class="sxs-lookup"><span data-stu-id="88edb-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="88edb-121">En este método, el reproductor proporciona un **valor HRESULT** para indicar si la descarga se ha realizado correctamente o no, el identificador de la pista y la cadena de parámetros personalizados que la tienda en línea proporcionó al llamar a **DownloadTrack**.</span><span class="sxs-lookup"><span data-stu-id="88edb-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88edb-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88edb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88edb-123">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="88edb-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




