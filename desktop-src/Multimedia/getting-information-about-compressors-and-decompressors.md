---
title: Obtener información acerca de los compresores y descompresores
description: Obtener información acerca de los compresores y descompresores
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Administrador de compresión de vídeo (VCM), obtener información sobre los compresores
- VCM (Administrador de compresión de vídeo), obtener información sobre los compresores
- ICGetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994273"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="b713e-106">Obtener información acerca de los compresores y descompresores</span><span class="sxs-lookup"><span data-stu-id="b713e-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="b713e-107">Para obtener información general sobre un compresor o descompresor, la aplicación puede usar la función [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) .</span><span class="sxs-lookup"><span data-stu-id="b713e-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="b713e-108">Esta función rellena una estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) con información sobre el compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="b713e-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="b713e-109">La aplicación debe asignar la memoria de la estructura **ICINFO** y pasar un puntero a ella en **ICGetInfo**.</span><span class="sxs-lookup"><span data-stu-id="b713e-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="b713e-110">A menos que la aplicación busque un compresor o descompresor determinado, las marcas de la estructura **ICINFO** proporcionan la información más útil sobre las capacidades de un compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="b713e-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="b713e-111">Para obtener la velocidad de fotogramas clave y el valor de calidad predeterminados de un compresor o descompresor, la aplicación puede enviar los mensajes [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) y [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (o usar las macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) y [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).</span><span class="sxs-lookup"><span data-stu-id="b713e-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="b713e-112">Para determinar el mejor formato de presentación de un compresor o descompresor, la aplicación puede usar la función [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .</span><span class="sxs-lookup"><span data-stu-id="b713e-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="b713e-113">Para determinar si un compresor o descompresor puede mostrar un cuadro de diálogo acerca de, envíe el mensaje [**ICM \_ About**](icm-about.md) (o use la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ).</span><span class="sxs-lookup"><span data-stu-id="b713e-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="b713e-114">También puede mostrar el cuadro de diálogo acerca de de un compresor o descompresor enviando el \_ mensaje ICM about y cambiando el valor del parámetro *wParam* (o mediante la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).</span><span class="sxs-lookup"><span data-stu-id="b713e-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




