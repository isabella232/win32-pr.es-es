---
title: Marca de prueba
description: Marca de prueba
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357735"
---
# <a name="the-test-flag"></a><span data-ttu-id="ca645-104">Marca de prueba</span><span class="sxs-lookup"><span data-stu-id="ca645-104">The Test Flag</span></span>

<span data-ttu-id="ca645-105">La marca "prueba" ( \_ prueba de MCI) consulta el dispositivo para determinar si puede ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="ca645-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="ca645-106">El dispositivo devuelve un error si no puede ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="ca645-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="ca645-107">No devuelve ningún error si puede controlar el comando.</span><span class="sxs-lookup"><span data-stu-id="ca645-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="ca645-108">Cuando se especifica esta marca, MCI devuelve el control a la aplicación sin ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="ca645-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="ca645-109">Esta marca es compatible con dispositivos digitales y vídeo VCR para todos los comandos excepto [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)) y [**cerrar**](close.md) ([**MCI \_ Close**](mci-close.md)).</span><span class="sxs-lookup"><span data-stu-id="ca645-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




