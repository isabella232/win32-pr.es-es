---
title: método Unload
description: método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790587"
---
# <a name="unload-method"></a><span data-ttu-id="bac95-103">método Unload</span><span class="sxs-lookup"><span data-stu-id="bac95-103">Unload Method</span></span>

<span data-ttu-id="bac95-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bac95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bac95-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="bac95-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bac95-106">Descarga los datos de caracteres para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="bac95-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="bac95-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="bac95-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bac95-108">*agente ***. Characters. UNLOAD "*** CharacterID \* *"**</span><span class="sxs-lookup"><span data-stu-id="bac95-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bac95-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bac95-109">Remarks</span></span>

<span data-ttu-id="bac95-110">Utilice este método cuando ya no necesite un carácter, para liberar memoria que se utiliza para almacenar información sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="bac95-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="bac95-111">Si vuelve a tener acceso al carácter, utilice el método [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="bac95-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="bac95-112">Este método no devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="bac95-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 