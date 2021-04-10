---
description: Este atributo agrega el icono de elevación de control de cuentas de usuario (UAC) al control PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156636"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="a87b8-103">Atributo ElevationShield</span><span class="sxs-lookup"><span data-stu-id="a87b8-103">ElevationShield Attribute</span></span>

<span data-ttu-id="a87b8-104">Este atributo agrega el icono de elevación de [*control de cuentas de usuario*](u-gly.md) (UAC) al [control Pushbutton](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="a87b8-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="a87b8-105">Si se establece este bit y la instalación todavía no se ejecuta con privilegios [*elevados*](e-gly.md) , el control Pushbutton se crea con el icono de elevación de [*control de cuentas de usuario*](u-gly.md) (UAC) (icono de escudo).</span><span class="sxs-lookup"><span data-stu-id="a87b8-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="a87b8-106">Si se establece este bit y la instalación ya se está ejecutando con privilegios [*elevados*](e-gly.md) , el control Pushbutton se crea con los demás atributos de icono.</span><span class="sxs-lookup"><span data-stu-id="a87b8-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="a87b8-107">Si no se establece este bit, el control Pushbutton se crea con los demás atributos de icono.</span><span class="sxs-lookup"><span data-stu-id="a87b8-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a87b8-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="a87b8-108">Valid Controls</span></span>

[<span data-ttu-id="a87b8-109">Botones</span><span class="sxs-lookup"><span data-stu-id="a87b8-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="a87b8-110">Value</span><span class="sxs-lookup"><span data-stu-id="a87b8-110">Value</span></span>



| <span data-ttu-id="a87b8-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="a87b8-111">Decimal</span></span> | <span data-ttu-id="a87b8-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="a87b8-112">Hexadecimal</span></span> | <span data-ttu-id="a87b8-113">Constante</span><span class="sxs-lookup"><span data-stu-id="a87b8-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="a87b8-114">8388608</span><span class="sxs-lookup"><span data-stu-id="a87b8-114">8388608</span></span> | <span data-ttu-id="a87b8-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="a87b8-115">0x00800000</span></span>  | <span data-ttu-id="a87b8-116">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="a87b8-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



