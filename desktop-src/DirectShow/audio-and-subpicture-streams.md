---
description: Secuencias de audio y subimagen
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Secuencias de audio y subimagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495653"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="03de1-103">Secuencias de audio y subimagen</span><span class="sxs-lookup"><span data-stu-id="03de1-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="03de1-104">Un disco DVD-Video puede tener hasta ocho flujos de audio, numerados de cero a siete, cada uno con hasta seis canales discretos.</span><span class="sxs-lookup"><span data-stu-id="03de1-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="03de1-105">(Tenga en cuenta que los flujos de audio y de subimagen se numeran desde cero, mientras que los títulos, los ángulos y los niveles parentales se numeran a partir de uno). Solo se puede seleccionar una de estas secuencias en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="03de1-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="03de1-106">En el caso de las subimágenes, hay hasta 32 secuencias disponibles, aunque solo se puede activar un flujo en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="03de1-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="03de1-107">Normalmente, los discos se crean con secuencias de audio y subimágenes predeterminadas, pero una aplicación puede permitir a los usuarios ver una lista de todas las secuencias disponibles y seleccionar la del lenguaje que prefieran.</span><span class="sxs-lookup"><span data-stu-id="03de1-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="03de1-108">Los pasos básicos de este proceso son los mismos para las secuencias de audio y de subimagen.</span><span class="sxs-lookup"><span data-stu-id="03de1-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="03de1-109">Determine el número de secuencias disponibles para un título.</span><span class="sxs-lookup"><span data-stu-id="03de1-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="03de1-110">Recorra en iteración los flujos y recupere los atributos de secuencia para cada uno.</span><span class="sxs-lookup"><span data-stu-id="03de1-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="03de1-111">Recupera el código de idioma del identificador de configuración regional (LCID) devuelto y crea una cadena legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="03de1-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="03de1-112">Rellene un cuadro de lista u otro control de la interfaz de usuario para permitir que el usuario seleccione una secuencia preferida.</span><span class="sxs-lookup"><span data-stu-id="03de1-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="03de1-113">En la aplicación de ejemplo de DVD, el método CAudioLangDlg:: MakeAudioStreamList de DIALOGS. cpp muestra los pasos básicos.</span><span class="sxs-lookup"><span data-stu-id="03de1-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03de1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03de1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03de1-115">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="03de1-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



