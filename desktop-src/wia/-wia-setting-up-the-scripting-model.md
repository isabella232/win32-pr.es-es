---
description: Para usar el modelo de scripting de adquisición de imágenes de Windows (WIA), debe tener el archivo Wiascr.dll instalado y registrado en el equipo.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurar el entorno de desarrollo del modelo de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275453"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="cc6e0-103">Configurar el entorno de desarrollo del modelo de scripting</span><span class="sxs-lookup"><span data-stu-id="cc6e0-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="cc6e0-104">Para usar el modelo de scripting de adquisición de imágenes de Windows (WIA), debe tener el archivo Wiascr.dll instalado y registrado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="cc6e0-105">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="cc6e0-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="cc6e0-106">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="cc6e0-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="cc6e0-107">Copie este archivo desde el SDK de WIA en el directorio *% WINDIR%*/system32 (por ejemplo, c: \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="cc6e0-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="cc6e0-108">En la línea de comandos, vaya a este directorio y escriba **regsvr32 Wiascr.dll**.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="cc6e0-109">Esto especifica la información necesaria en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="cc6e0-110">Ahora está listo para usar el modelo de scripting de WIA.</span><span class="sxs-lookup"><span data-stu-id="cc6e0-110">You are now ready to use the WIA scripting model.</span></span>

 

 
