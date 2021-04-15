---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador impide que los usuarios que no sean administradores usen la aplicación de revisiones del control de cuentas de usuario (UAC) para cualquier aplicación instalada en el equipo.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669999"
---
# <a name="disableluapatching"></a><span data-ttu-id="1b714-103">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="1b714-103">DisableLUAPatching</span></span>

<span data-ttu-id="1b714-104">Si esta Directiva del sistema por equipo se establece en "1", el instalador impide que los usuarios que no sean administradores utilicen la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para cualquier aplicación instalada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="1b714-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="1b714-105">Cuando la Directiva del sistema por equipo no se establece o se establece en 0, los usuarios que no son administradores pueden aplicar revisiones de usuario con privilegios mínimos a las aplicaciones habilitadas para la aplicación de revisiones de cuenta de usuario con privilegios mínimos.</span><span class="sxs-lookup"><span data-stu-id="1b714-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="1b714-106">Use la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) para evitar la aplicación de revisiones con privilegios mínimos de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b714-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="1b714-107">La Directiva DisableLUAPatching está disponible a partir de Windows Installer versión 3,0.</span><span class="sxs-lookup"><span data-stu-id="1b714-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="1b714-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="1b714-108">Registry Key</span></span>

<span data-ttu-id="1b714-109">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="1b714-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="1b714-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1b714-110">Data Type</span></span>

<span data-ttu-id="1b714-111">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="1b714-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b714-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b714-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b714-113">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="1b714-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



