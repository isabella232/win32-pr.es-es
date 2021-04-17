---
description: WIA proporciona una capa de compatibilidad de TWAIN que permite a las aplicaciones compatibles con TWAIN comunicarse con dispositivos de adquisición de imágenes de Windows (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilidad con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696507"
---
# <a name="twain-compatibility"></a><span data-ttu-id="e5827-103">Compatibilidad con TWAIN</span><span class="sxs-lookup"><span data-stu-id="e5827-103">TWAIN Compatibility</span></span>

<span data-ttu-id="e5827-104">WIA proporciona una capa de compatibilidad de TWAIN que permite a las aplicaciones compatibles con TWAIN comunicarse con dispositivos de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="e5827-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="e5827-105">Las aplicaciones que reconocen TWAIN no tienen acceso total a la funcionalidad de WIA.</span><span class="sxs-lookup"><span data-stu-id="e5827-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="e5827-106">Por ejemplo, una aplicación no puede suprimir la interfaz de usuario mediante el nivel de compatibilidad TWAIN.</span><span class="sxs-lookup"><span data-stu-id="e5827-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="e5827-107">Los dispositivos WIA aparecen dos veces en una aplicación que es consciente de WIA y TWAIN: una vez a través de una comunicación WIA normal y otra a través de la capa de compatibilidad TWAIN.</span><span class="sxs-lookup"><span data-stu-id="e5827-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="e5827-108">Para evitar que se muestren dos veces un dispositivo WIA, una aplicación que tenga en cuenta WIA y TWAIN debe filtrar los dispositivos WIA que provienen del nivel de compatibilidad TWAIN.</span><span class="sxs-lookup"><span data-stu-id="e5827-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="e5827-109">Todos los dispositivos WIA que atraviesan el nivel de compatibilidad TWAIN tienen "WIA-" como prefijo, por lo que es fácil filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="e5827-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



