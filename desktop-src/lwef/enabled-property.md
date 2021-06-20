---
title: Propiedad Enabled (objeto Balloon)
description: Obtenga información sobre la propiedad del objeto Globo habilitado. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407308"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="5dc4a-104">Propiedad Enabled (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="5dc4a-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="5dc4a-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5dc4a-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5dc4a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5dc4a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5dc4a-107">Devuelve si el globo de palabras está habilitado para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="5dc4a-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="5dc4a-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5dc4a-109">*agent\***. Caracteres ("**_CharacterID_*_"). Balloon.Enabled_\*</span><span class="sxs-lookup"><span data-stu-id="5dc4a-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="5dc4a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5dc4a-110">Value</span></span>     | <span data-ttu-id="5dc4a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dc4a-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="5dc4a-112">**True**</span><span class="sxs-lookup"><span data-stu-id="5dc4a-112">**True**</span></span>  | <span data-ttu-id="5dc4a-113">El globo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="5dc4a-114">**False**</span><span class="sxs-lookup"><span data-stu-id="5dc4a-114">**False**</span></span> | <span data-ttu-id="5dc4a-115">El globo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dc4a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dc4a-116">Remarks</span></span>

<span data-ttu-id="5dc4a-117">La **propiedad Enabled** devuelve un valor booleano que especifica si el globo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="5dc4a-118">El estado predeterminado del globo de palabras se establece como parte de la definición de un carácter cuando el carácter se compila en el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="5dc4a-119">Si se define un carácter para no admitir el globo de palabras, esta propiedad siempre será **False** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="5dc4a-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




