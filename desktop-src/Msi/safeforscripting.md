---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador no solicitará a los usuarios que los scripts de una página web usen la interfaz de automatización del instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666794"
---
# <a name="safeforscripting"></a><span data-ttu-id="6ec74-103">SafeForScripting</span><span class="sxs-lookup"><span data-stu-id="6ec74-103">SafeForScripting</span></span>

<span data-ttu-id="6ec74-104">Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador no solicitará a los usuarios cuando los scripts de una página web utilicen la [interfaz de automatización](automation-interface.md)del instalador.</span><span class="sxs-lookup"><span data-stu-id="6ec74-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="6ec74-105">Antes de establecer esta Directiva, debe considerar si, antes de la solicitud del usuario, se proporciona un nivel de seguridad adecuado para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="6ec74-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="6ec74-106">Si no se establece esta Directiva, cuando un script hospedado por un explorador de Internet intenta instalar una aplicación, el sistema advierte al usuario y le pide que acepte o rechace la instalación.</span><span class="sxs-lookup"><span data-stu-id="6ec74-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="6ec74-107">La configuración de SafeForScripting suprime esta advertencia y puede permitir la instalación de aplicaciones en el sistema sin el conocimiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ec74-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="6ec74-108">Esta Directiva puede ser útil para una empresa que usa herramientas basadas en web para distribuir programas.</span><span class="sxs-lookup"><span data-stu-id="6ec74-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="6ec74-109">Para obtener más información, consulte [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y [descargar una instalación desde Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="6ec74-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="6ec74-110">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="6ec74-110">Registry Key</span></span>

<span data-ttu-id="6ec74-111">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="6ec74-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="6ec74-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6ec74-112">Data Type</span></span>

<span data-ttu-id="6ec74-113">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6ec74-113">**REG\_DWORD**</span></span>

 

 



