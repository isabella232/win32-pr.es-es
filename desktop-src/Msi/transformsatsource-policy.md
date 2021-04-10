---
description: Si esta Directiva del sistema por usuario está establecida en &\# 0034; 1&\# 0034;; el instalador busca los archivos de transformación en la raíz de los orígenes de red de la lista de origen del producto. De forma predeterminada, las transformaciones se almacenan en la carpeta datos de la aplicación del perfil de un usuario.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Directiva TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153741"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="334f6-104">Directiva TransformsAtSource</span><span class="sxs-lookup"><span data-stu-id="334f6-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="334f6-105">Si esta [Directiva del sistema](system-policy.md) por usuario está establecida en "1"; el instalador busca los archivos de transformación en la raíz de los orígenes de red de la lista de origen del producto.</span><span class="sxs-lookup"><span data-stu-id="334f6-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="334f6-106">De forma predeterminada, las transformaciones se almacenan en la carpeta datos de la aplicación del perfil de un usuario.</span><span class="sxs-lookup"><span data-stu-id="334f6-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="334f6-107">Windows Installer interpreta que la Directiva TransformsAtSource es la misma que la [Directiva TransformsSecure](transformssecure-policy.md).</span><span class="sxs-lookup"><span data-stu-id="334f6-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="334f6-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="334f6-108">Registry Key</span></span>

<span data-ttu-id="334f6-109">**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="334f6-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="334f6-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="334f6-110">Data Type</span></span>

<span data-ttu-id="334f6-111">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="334f6-111">**REG\_SZ**</span></span>

 

 



