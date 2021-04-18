---
description: Las API de adquisición de imágenes de Windows (WIA) devuelven el estado de finalización en un valor devuelto HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Información de error de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715178"
---
# <a name="wia-error-information"></a><span data-ttu-id="4da82-103">Información de error de WIA</span><span class="sxs-lookup"><span data-stu-id="4da82-103">WIA Error Information</span></span>

<span data-ttu-id="4da82-104">Las API de adquisición de imágenes de Windows (WIA) devuelven el estado de finalización en un valor devuelto HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4da82-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="4da82-105">Las aplicaciones comprueban estos valores devueltos con la \_ constante de WIA de instalación para determinar si el error requiere la intervención del usuario para borrar, como una ruta de papel atascada, y notificarlos al usuario.</span><span class="sxs-lookup"><span data-stu-id="4da82-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="4da82-106">Además, todos los errores de nivel de controlador se registran en detalle en el registro de eventos, con las cadenas de error proporcionadas por el minicontrolador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4da82-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="4da82-107">Para obtener una lista de códigos de error específicos de WIA, consulte [códigos de error](-wia-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4da82-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 



