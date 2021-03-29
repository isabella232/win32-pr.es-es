---
title: Remove (método)
description: Remove (método)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358974"
---
# <a name="remove-method"></a><span data-ttu-id="c7278-103">Remove (método)</span><span class="sxs-lookup"><span data-stu-id="c7278-103">Remove Method</span></span>

<span data-ttu-id="c7278-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7278-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c7278-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="c7278-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c7278-106">Quita un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c7278-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="c7278-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="c7278-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c7278-108">*agente ***. Caracteres ("*** CharacterID ***"). Commands. Remove*** Name*</span><span class="sxs-lookup"><span data-stu-id="c7278-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="c7278-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c7278-109">Part</span></span>   | <span data-ttu-id="c7278-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7278-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="c7278-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="c7278-111">*Name*</span></span> | <span data-ttu-id="c7278-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7278-112">Required.</span></span> <span data-ttu-id="c7278-113">Valor de cadena que corresponde al identificador del comando.</span><span class="sxs-lookup"><span data-stu-id="c7278-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7278-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7278-114">Remarks</span></span>

<span data-ttu-id="c7278-115">Cuando se quita un objeto de [**comando**](/windows/desktop/lwef/the-command-object) de la colección, ya no aparece cuando se muestra el menú emergente del carácter o en la ventana comandos cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="c7278-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7278-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c7278-116">See Also</span></span>

[<span data-ttu-id="c7278-117">**método RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="c7278-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 