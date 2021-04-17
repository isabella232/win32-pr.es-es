---
title: Control de errores con funciones de audio
description: Control de errores con funciones de audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimedia, errores de audio de onda
- audio, errores de audio de onda
- audio multimedia, errores de audio auxiliar
- audio, errores de audio auxiliar
- audio de la onda, errores
- audio auxiliar, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358857"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="cac56-109">Control de errores con funciones de audio</span><span class="sxs-lookup"><span data-stu-id="cac56-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="cac56-110">Las funciones de audio de onda y de audio auxiliar devuelven un valor distinto de cero cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cac56-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="cac56-111">Windows proporciona funciones que convierten estos valores de error en descripciones textuales de los errores.</span><span class="sxs-lookup"><span data-stu-id="cac56-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="cac56-112">La aplicación debe seguir examinando los valores de error para determinar cómo proceder, pero se pueden usar descripciones de texto de los errores en los cuadros de diálogo que describen los errores para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cac56-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="cac56-113">Puede utilizar las siguientes funciones para recuperar descripciones textuales de los valores de error de audio:</span><span class="sxs-lookup"><span data-stu-id="cac56-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="cac56-114">Función</span><span class="sxs-lookup"><span data-stu-id="cac56-114">Function</span></span>                                           | <span data-ttu-id="cac56-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="cac56-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="cac56-116">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="cac56-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="cac56-117">Recupera una descripción textual de un error de entrada de audio de onda especificada.</span><span class="sxs-lookup"><span data-stu-id="cac56-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="cac56-118">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="cac56-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="cac56-119">Recupera una descripción textual de un error de salida de onda de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="cac56-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="cac56-120">Las únicas funciones de audio que no devuelven valores de error son [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)y [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span><span class="sxs-lookup"><span data-stu-id="cac56-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="cac56-121">Estas funciones devuelven cero si no hay ningún dispositivo presente en un sistema o si encuentran errores.</span><span class="sxs-lookup"><span data-stu-id="cac56-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 