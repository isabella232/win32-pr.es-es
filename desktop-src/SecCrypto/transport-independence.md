---
description: Los certificados se pueden solicitar y distribuir a través de cualquier mecanismo de transporte.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Independencia de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648233"
---
# <a name="transport-independence"></a><span data-ttu-id="049f4-103">Independencia de transporte</span><span class="sxs-lookup"><span data-stu-id="049f4-103">Transport Independence</span></span>

<span data-ttu-id="049f4-104">Los certificados se pueden solicitar y distribuir a través de cualquier mecanismo de transporte.</span><span class="sxs-lookup"><span data-stu-id="049f4-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="049f4-105">Los servicios de Certificate Server aceptan [*solicitudes de certificado*](../secgloss/c-gly.md) de un solicitante a través de http, DCOM, RPC, un archivo de disco o un transporte personalizado.</span><span class="sxs-lookup"><span data-stu-id="049f4-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="049f4-106">Servicios de Certificate Server envía certificados al solicitante a través de HTTP, DCOM, RPC, un archivo de disco o un transporte personalizado.</span><span class="sxs-lookup"><span data-stu-id="049f4-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="049f4-107">Los transportes son compatibles con las aplicaciones intermediarios y los archivos DLL del módulo de salida, que normalmente se escriben en C/C++.</span><span class="sxs-lookup"><span data-stu-id="049f4-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="049f4-108">Las aplicaciones intermediarios y los módulos de salida aíslan las funciones de servicios de Certificate Server de comunicarse con cualquier transporte específico.</span><span class="sxs-lookup"><span data-stu-id="049f4-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
