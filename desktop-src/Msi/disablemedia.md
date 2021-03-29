---
description: Si esta Directiva del sistema por usuario está establecida en &\# 0034; 1&\# 0034;, los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para buscar orígenes multimedia, como un CD-ROM, para los orígenes de otros productos instalables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003306"
---
# <a name="disablemedia"></a><span data-ttu-id="89f1a-103">DisableMedia</span><span class="sxs-lookup"><span data-stu-id="89f1a-103">DisableMedia</span></span>

<span data-ttu-id="89f1a-104">Si esta [Directiva del sistema](system-policy.md) por usuario se establece en "1", los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para examinar los orígenes multimedia, como el CD-ROM, para los orígenes de otros productos instalables.</span><span class="sxs-lookup"><span data-stu-id="89f1a-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="89f1a-105">La exploración de otros productos se evita independientemente de si la instalación se realiza con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="89f1a-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="89f1a-106">Todavía es posible que el usuario vuelva a instalar el producto desde el medio si el usuario tiene un origen de medios correctamente etiquetado.</span><span class="sxs-lookup"><span data-stu-id="89f1a-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="89f1a-107">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="89f1a-107">Registry Key</span></span>

<span data-ttu-id="89f1a-108">**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="89f1a-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="89f1a-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="89f1a-109">Data Type</span></span>

<span data-ttu-id="89f1a-110">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="89f1a-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="89f1a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89f1a-111">Remarks</span></span>

<span data-ttu-id="89f1a-112">Tenga en cuenta que la propiedad [**DISABLEMEDIA**](-disablemedia.md) tiene un efecto distinto al de la Directiva DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="89f1a-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="89f1a-113">Al establecer la Directiva del sistema DisableMedia, solo se deshabilita la exploración de los orígenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="89f1a-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="89f1a-114">El establecimiento de la propiedad **DISABLEMEDIA** evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.</span><span class="sxs-lookup"><span data-stu-id="89f1a-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="89f1a-115">Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="89f1a-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f1a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89f1a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f1a-117">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="89f1a-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



