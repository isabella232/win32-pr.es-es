---
title: Insert (método)
description: Insert (método)
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685704"
---
# <a name="insert-method"></a><span data-ttu-id="2a327-103">Insert (método)</span><span class="sxs-lookup"><span data-stu-id="2a327-103">Insert Method</span></span>

<span data-ttu-id="2a327-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a327-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2a327-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="2a327-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2a327-106">Inserta un objeto **Command** en la colección **Commands** .</span><span class="sxs-lookup"><span data-stu-id="2a327-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="2a327-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="2a327-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2a327-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Commands. Insert* \*  *Name*, *RefName*, *Before*\_</span><span class="sxs-lookup"><span data-stu-id="2a327-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="2a327-109">*Título*, *voz, habilitado, visible*</span><span class="sxs-lookup"><span data-stu-id="2a327-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="2a327-110">Parte</span><span class="sxs-lookup"><span data-stu-id="2a327-110">Part</span></span>      | <span data-ttu-id="2a327-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a327-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a327-112">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="2a327-112">*Name*</span></span>    | <span data-ttu-id="2a327-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a327-113">Required.</span></span> <span data-ttu-id="2a327-114">Valor de cadena que corresponde al identificador que se asigna al [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="2a327-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="2a327-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="2a327-115">*RefName*</span></span> | <span data-ttu-id="2a327-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a327-116">Required.</span></span> <span data-ttu-id="2a327-117">Un valor de cadena que corresponde al nombre (ID.) del comando justo encima o debajo del lugar en el que desea insertar el nuevo comando.</span><span class="sxs-lookup"><span data-stu-id="2a327-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="2a327-118">*Antes*</span><span class="sxs-lookup"><span data-stu-id="2a327-118">*Before*</span></span>  | <span data-ttu-id="2a327-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a327-119">Optional.</span></span> <span data-ttu-id="2a327-120">Valor booleano que indica si se va a insertar el nuevo comando antes del comando especificado por *RefName*.</span><span class="sxs-lookup"><span data-stu-id="2a327-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="2a327-121">**True** (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2a327-121">**True** (Default).</span></span> <span data-ttu-id="2a327-122">El nuevo comando se insertará antes del comando al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="2a327-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="2a327-123">**False** El nuevo comando se insertará después del comando al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="2a327-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="2a327-124">*Caption*</span><span class="sxs-lookup"><span data-stu-id="2a327-124">*Caption*</span></span> | <span data-ttu-id="2a327-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a327-125">Optional.</span></span> <span data-ttu-id="2a327-126">Un valor de cadena que corresponde al nombre que aparecerá en el menú emergente del carácter y en la ventana comandos cuando la aplicación cliente sea de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="2a327-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="2a327-127">Para obtener más información, vea la propiedad [**Caption**](caption-property.md)del objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="2a327-128">*Voz*</span><span class="sxs-lookup"><span data-stu-id="2a327-128">*Voice*</span></span>   | <span data-ttu-id="2a327-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a327-129">Optional.</span></span> <span data-ttu-id="2a327-130">Valor de cadena que corresponde a las palabras o la frase que va a usar el motor de voz para reconocer este comando.</span><span class="sxs-lookup"><span data-stu-id="2a327-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="2a327-131">Para obtener más información sobre las alternativas de formato de la cadena, vea la propiedad **Voice** del objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="2a327-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="2a327-132">*Enabled*</span></span> | <span data-ttu-id="2a327-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a327-133">Optional.</span></span> <span data-ttu-id="2a327-134">Valor booleano que indica si el comando está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2a327-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="2a327-135">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="2a327-135">The default value is **True**.</span></span> <span data-ttu-id="2a327-136">Para obtener más información, vea la propiedad **Enabled** del objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="2a327-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="2a327-137">*Visible*</span></span> | <span data-ttu-id="2a327-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2a327-138">Optional.</span></span> <span data-ttu-id="2a327-139">Un valor booleano que indica si el comando está visible en la ventana comandos cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="2a327-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="2a327-140">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="2a327-140">The default value is **True**.</span></span> <span data-ttu-id="2a327-141">Para obtener más información, vea la propiedad [**visible**](visible-property.md) del objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a327-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a327-142">Remarks</span></span>

<span data-ttu-id="2a327-143">El valor de la propiedad [**Name**](name-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) debe ser único dentro de su colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="2a327-144">Debe quitar un **comando** para poder crear un nuevo **comando** con el mismo valor de la propiedad **nombre** .</span><span class="sxs-lookup"><span data-stu-id="2a327-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="2a327-145">Al intentar crear un **comando** con una propiedad **Name** que ya existe, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a327-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="2a327-146">Este método también devuelve un objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2a327-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="2a327-147">Esto permite declarar un objeto y asignarle un **comando** cuando se llama al método **Insert** .</span><span class="sxs-lookup"><span data-stu-id="2a327-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="2a327-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a327-148">See Also</span></span>

<span data-ttu-id="2a327-149">[**Método Add**](add-method.md), [**Remove Method**](remove-method.md), [**RemoveAll Method**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="2a327-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

