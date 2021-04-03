---
description: La versión de depuración del motor de XAudio2 valida los parámetros y proporciona mensajes de advertencia y error detallados.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Funciones de depuración de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810459"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="87a3d-103">Funciones de depuración de XAudio2</span><span class="sxs-lookup"><span data-stu-id="87a3d-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="87a3d-104">La versión de depuración del motor de XAudio2 valida los parámetros y proporciona mensajes de advertencia y error detallados.</span><span class="sxs-lookup"><span data-stu-id="87a3d-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="87a3d-105">Establecer el nivel de registro de depuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="87a3d-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="87a3d-106">Puede establecer el nivel de información de depuración que se muestra en XAudio2 en cualquier momento rellenando una estructura de [**\_ \_ configuración de depuración xaudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con las marcas para el nivel de registro deseado y, después, pasar la estructura al método [**IXAudio2:: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="87a3d-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="87a3d-107">Los valores que se pasan al método **IXAudio2:: SetDebugConfiguration** siempre invalidan los valores predeterminados que se establecieron en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="87a3d-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="87a3d-108">Compatibilidad con depuración</span><span class="sxs-lookup"><span data-stu-id="87a3d-108">Debug Support</span></span>

<span data-ttu-id="87a3d-109">Las funciones de depuración siempre están disponibles para XAUDIO2 en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87a3d-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="87a3d-110">En el caso de las versiones del SDK de DirectX de XAUDIO2, debe usar el **\_ \_ motor de depuración xaudio2** al crear el objeto xaudio2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) y el sistema debe tener instalado el entorno de tiempo de ejecución para desarrolladores de DirectX SDK para que se admita la depuración.</span><span class="sxs-lookup"><span data-stu-id="87a3d-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87a3d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87a3d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87a3d-112">Funciones de depuración</span><span class="sxs-lookup"><span data-stu-id="87a3d-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="87a3d-113">Referencia de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="87a3d-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
