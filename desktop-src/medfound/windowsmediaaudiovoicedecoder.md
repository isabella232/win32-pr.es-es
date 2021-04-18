---
description: El descodificador de voz de Windows Media Audio descodifica los flujos codificados por el codificador de Windows Media Audio Voice.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Descodificador de Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699554"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="c2f2c-103">Descodificador de Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="c2f2c-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="c2f2c-104">El descodificador de voz de Windows Media Audio descodifica los flujos codificados por el [**codificador de Windows Media Audio Voice**](windowsmediaaudiovoiceencoder.md).</span><span class="sxs-lookup"><span data-stu-id="c2f2c-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="c2f2c-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="c2f2c-105">Class Identifier</span></span>

<span data-ttu-id="c2f2c-106">El identificador de clase (CLSID) para el descodificador de Windows Media Audio Voice se representa mediante la **constante \_ CWMSPDecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="c2f2c-107">Puede crear una instancia del descodificador de voz llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="c2f2c-108">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="c2f2c-108">Input Formats</span></span>

<span data-ttu-id="c2f2c-109">Windows Media Audio contenido codificado por voz se identifica mediante la etiqueta de formato 0x00A.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f2c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f2c-110">Requirements</span></span>



| <span data-ttu-id="c2f2c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f2c-111">Requirement</span></span> | <span data-ttu-id="c2f2c-112">Value</span><span class="sxs-lookup"><span data-stu-id="c2f2c-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f2c-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="c2f2c-113">Client</span></span><br/> | <span data-ttu-id="c2f2c-114">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2f2c-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="c2f2c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2f2c-115">Header</span></span><br/> | <dl> <span data-ttu-id="c2f2c-116"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2f2c-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="c2f2c-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2f2c-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="c2f2c-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2f2c-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2f2c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2f2c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f2c-120">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="c2f2c-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="c2f2c-121">Usar el códec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="c2f2c-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="c2f2c-122">Codificador de voz Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="c2f2c-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




