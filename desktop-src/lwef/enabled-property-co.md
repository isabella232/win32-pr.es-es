---
title: Propiedad Enabled (objeto Command)
description: Propiedad Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695825"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="705cd-103">Propiedad Enabled (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="705cd-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="705cd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="705cd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="705cd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="705cd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="705cd-106">Devuelve o establece si el **comando** está habilitado en el menú emergente del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="705cd-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="705cd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="705cd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="705cd-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Comandos ("_*_Name_\*_"). Booleano habilitado_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="705cd-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="705cd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="705cd-109">Part</span></span>      | <span data-ttu-id="705cd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="705cd-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705cd-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="705cd-111">*boolean*</span></span> | <span data-ttu-id="705cd-112">Una expresión booleana que especifica si el **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="705cd-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="705cd-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="705cd-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="705cd-114">El **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="705cd-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="705cd-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="705cd-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="705cd-116">El **comando** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="705cd-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="705cd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="705cd-117">Remarks</span></span>

<span data-ttu-id="705cd-118">Si la propiedad [**Enabled**](enabled-property.md) está establecida en **true**, el título de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) aparece como texto normal en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="705cd-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="705cd-119">Si la propiedad **Enabled** es **false**, el título aparece como texto no disponible (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="705cd-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="705cd-120">Tampoco se puede obtener acceso a un **comando** deshabilitado para la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="705cd-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

