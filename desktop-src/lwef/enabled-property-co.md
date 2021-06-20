---
title: Propiedad Enabled (objeto Command)
description: Obtenga información sobre la propiedad de objeto Enabled Command. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407338"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="187e9-104">Propiedad Enabled (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="187e9-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="187e9-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="187e9-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="187e9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="187e9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="187e9-107">Devuelve o establece si el **comando** está habilitado en el menú emergente del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="187e9-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="187e9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="187e9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="187e9-109">*agent\***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Booleano_ \*  \[  =  *habilitado*\]</span><span class="sxs-lookup"><span data-stu-id="187e9-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="187e9-110">Parte</span><span class="sxs-lookup"><span data-stu-id="187e9-110">Part</span></span>      | <span data-ttu-id="187e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="187e9-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187e9-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="187e9-112">*boolean*</span></span> | <span data-ttu-id="187e9-113">Expresión booleana que especifica si el **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="187e9-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="187e9-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdad**</dt></span><span class="sxs-lookup"><span data-stu-id="187e9-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="187e9-115">El **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="187e9-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="187e9-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt></span><span class="sxs-lookup"><span data-stu-id="187e9-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="187e9-117">El **comando** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="187e9-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="187e9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="187e9-118">Remarks</span></span>

<span data-ttu-id="187e9-119">Si la [**propiedad Enabled**](enabled-property.md) está establecida en **True**, el título de los objetos [**Command**](/windows/desktop/lwef/the-command-object) aparece como texto normal en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada.</span><span class="sxs-lookup"><span data-stu-id="187e9-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="187e9-120">Si la **propiedad Enabled** es **False**, el título aparece como texto no disponible (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="187e9-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="187e9-121">Tampoco se **puede acceder a** un comando deshabilitado para la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="187e9-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

