---
description: Inserción de fotogramas clave forzada
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserción de fotogramas clave forzada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496810"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="f2278-103">Inserción de fotogramas clave forzada (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="f2278-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="f2278-104">Al configurar un objeto de codificador de vídeo, puede establecer un intervalo máximo para los fotogramas clave en el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="f2278-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="f2278-105">Sin embargo, el códec colocará fotogramas clave dentro de ese intervalo tal como lo indica el contenido; el intervalo de fotogramas clave no es constante.</span><span class="sxs-lookup"><span data-stu-id="f2278-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="f2278-106">En algunas aplicaciones, la distancia del fotograma clave es muy importante.</span><span class="sxs-lookup"><span data-stu-id="f2278-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="f2278-107">Por ejemplo, una aplicación de edición de vídeo necesita fotogramas clave en las ubicaciones que son lógicas para un editor, como en los saltos de escena y las transiciones de captura.</span><span class="sxs-lookup"><span data-stu-id="f2278-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="f2278-108">La inserción de fotogramas clave forzada es una característica que permite solicitar que un fotograma de entrada se codifique como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="f2278-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="f2278-109">El codificador tratará de cumplir estas solicitudes, pero la configuración de búfer (velocidad de bits y ventana de búfer) configurada para la sesión de codificación siempre tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="f2278-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="f2278-110">Los objetos del codificador de vídeo implementan la inserción del fotograma clave forzada como respuesta a una extensión de unidad de datos asociada a la muestra de entrada.</span><span class="sxs-lookup"><span data-stu-id="f2278-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="f2278-111">Para obtener más información acerca de las extensiones de unidad de datos, consulte [uso de extensiones de unidad de datos](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="f2278-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="f2278-112">Los datos de extensión para la inserción de fotogramas clave forzada se identifican mediante el siguiente valor de GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="f2278-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="f2278-113">Las extensiones individuales son valores **bool** .</span><span class="sxs-lookup"><span data-stu-id="f2278-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="f2278-114">Establezca el valor en **true** para indicar una solicitud de fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="f2278-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2278-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2278-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2278-116">Uso de extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="f2278-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="f2278-117">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="f2278-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



