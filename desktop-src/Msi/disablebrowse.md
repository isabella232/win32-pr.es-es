---
description: Al establecer el valor de esta Directiva del sistema por equipo en &\# 0034; 1&\# 0034; se impide que los usuarios no administrativos utilicen un cuadro de diálogo examinar para buscar orígenes de aplicaciones administradas almacenadas en medios, como un CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652371"
---
# <a name="disablebrowse"></a><span data-ttu-id="4f8d2-103">DisableBrowse</span><span class="sxs-lookup"><span data-stu-id="4f8d2-103">DisableBrowse</span></span>

<span data-ttu-id="4f8d2-104">Al establecer el valor de esta [Directiva del sistema](system-policy.md) por equipo en "1", se impide que los usuarios no administrativos utilicen un [cuadro de diálogo examinar](browse-dialog.md) para buscar orígenes de [*aplicaciones administradas*](m-gly.md) almacenadas en medios, como un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="4f8d2-105">El cuadro combinado "usar característica de:" para entrada directa está bloqueado y el "examinar..." el botón está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="4f8d2-106">Para obtener más información sobre la exploración de código fuente, consulte [resistencia de origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="4f8d2-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="4f8d2-107">DisableBrowse invalida AllowLockdownBrowse y evita que se examine incluso si AllowLockdownBrowse está establecido.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="4f8d2-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="4f8d2-108">Registry Key</span></span>

<span data-ttu-id="4f8d2-109">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="4f8d2-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="4f8d2-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4f8d2-110">Data Type</span></span>

<span data-ttu-id="4f8d2-111">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="4f8d2-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8d2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f8d2-112">Remarks</span></span>

<span data-ttu-id="4f8d2-113">En algunos casos con DisableBrowse establecido, un usuario no administrativo puede seguir pudiendo instalar aplicaciones administradas desde orígenes en medios etiquetados correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="4f8d2-114">La configuración de la Directiva DisableBrowse solo deshabilita la capacidad de examinar los orígenes.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="4f8d2-115">Se puede usar para impedir que un usuario no administrativo navegue a un nuevo origen durante una instalación, reinstalación o reparación a petición.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="4f8d2-116">Si se establece [AllowLockdownMedia](allowlockdownmedia.md) , el usuario no administrativo podría seguir instalando una aplicación administrada desde un medio etiquetado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="4f8d2-117">DisableBrowse impide que el usuario no administrativo navegue a una nueva ubicación de medios o a cualquier otra ubicación de origen.</span><span class="sxs-lookup"><span data-stu-id="4f8d2-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="4f8d2-118">Para obtener más información sobre cómo proteger los orígenes multimedia de las aplicaciones administradas, consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="4f8d2-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="4f8d2-119">Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="4f8d2-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



