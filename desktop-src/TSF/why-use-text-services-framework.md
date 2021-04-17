---
title: Por qué usar el marco de trabajo de servicios de texto
description: Por qué usar el marco de trabajo de servicios de texto
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- Marco de trabajo de servicios de texto (TSF), acerca de
- TSF (marco de trabajo de servicios de texto), acerca de
- servicios de texto, acerca de
- Aplicaciones habilitadas para TSF, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685482"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="37e84-107">¿Por qué usar el marco de trabajo de servicios de texto?</span><span class="sxs-lookup"><span data-stu-id="37e84-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="37e84-108">El marco de trabajo de servicios de texto (TSF) permite que una aplicación habilitada para TSF reciba entradas de texto de cualquier número de dispositivos o orígenes.</span><span class="sxs-lookup"><span data-stu-id="37e84-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="37e84-109">Dado que TSF es extensible, la aplicación puede recibir entradas de texto de orígenes de texto adicionales con poca o ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="37e84-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="37e84-110">Un servicio de texto obtiene texto de y proporciona texto a cualquier aplicación habilitada para TSF sin necesidad de ningún conocimiento sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37e84-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="37e84-111">Esta estructura permite que el servicio de texto esté disponible para cualquier aplicación habilitada para TSF.</span><span class="sxs-lookup"><span data-stu-id="37e84-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="37e84-112">El servicio de texto se puede instalar o actualizar como un módulo independiente y es independiente de cualquier aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="37e84-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="37e84-113">TSF también permite a un servicio de texto almacenar metadatos con un documento, un fragmento de texto o un objeto dentro del documento.</span><span class="sxs-lookup"><span data-stu-id="37e84-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="37e84-114">Por ejemplo, un servicio de texto de entrada de voz puede almacenar información de sonido asociada a un bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="37e84-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="37e84-115">TSF permite a los servicios de texto proporcionar una conversión de texto precisa y completa, con acceso continuo al búfer del documento.</span><span class="sxs-lookup"><span data-stu-id="37e84-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="37e84-116">Los servicios de texto que usan TSF pueden evitar separar su funcionalidad en modos de entrada y de modo de edición.</span><span class="sxs-lookup"><span data-stu-id="37e84-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="37e84-117">Esta arquitectura de entrada permite que el flujo de texto almacenado en búfer y acumulado Cambie dinámicamente, lo que permite una edición de texto y una entrada de teclado más eficientes.</span><span class="sxs-lookup"><span data-stu-id="37e84-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="37e84-118">TSF es independiente del dispositivo y habilita los servicios de texto para varios dispositivos de entrada, como el teclado, el lápiz y el micrófono.</span><span class="sxs-lookup"><span data-stu-id="37e84-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




