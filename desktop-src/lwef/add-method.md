---
title: Agregar método
description: Agregar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075610"
---
# <a name="add-method"></a><span data-ttu-id="9a345-103">Agregar método</span><span class="sxs-lookup"><span data-stu-id="9a345-103">Add Method</span></span>

<span data-ttu-id="9a345-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a345-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9a345-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="9a345-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9a345-106">Agrega un objeto [Command](the-command-object.md) a la colección [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="9a345-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="9a345-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9a345-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Comandos. agregar* \*  *nombre*, *título*, *voz*, *habilitado*, *visible*</span><span class="sxs-lookup"><span data-stu-id="9a345-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="9a345-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9a345-109">Part</span></span>      | <span data-ttu-id="9a345-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a345-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a345-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="9a345-111">*Name*</span></span>    | <span data-ttu-id="9a345-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a345-112">Required.</span></span> <span data-ttu-id="9a345-113">Valor de cadena que corresponde al identificador que se asigna para el comando.</span><span class="sxs-lookup"><span data-stu-id="9a345-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="9a345-114">*Caption*</span><span class="sxs-lookup"><span data-stu-id="9a345-114">*Caption*</span></span> | <span data-ttu-id="9a345-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a345-115">Optional.</span></span> <span data-ttu-id="9a345-116">Un valor de cadena que corresponde al nombre que aparecerá en el menú emergente del carácter y en la ventana comandos cuando la aplicación cliente sea de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="9a345-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="9a345-117">Para obtener más información, vea la propiedad [Caption](caption-property.md) del objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="9a345-118">*Voz*</span><span class="sxs-lookup"><span data-stu-id="9a345-118">*Voice*</span></span>   | <span data-ttu-id="9a345-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a345-119">Optional.</span></span> <span data-ttu-id="9a345-120">Valor de cadena que corresponde a las palabras o la frase que va a usar el motor de voz para reconocer este comando.</span><span class="sxs-lookup"><span data-stu-id="9a345-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="9a345-121">Para obtener más información sobre las alternativas de formato de la cadena, vea la propiedad [Voice](voice-property.md) del objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="9a345-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="9a345-122">*Enabled*</span></span> | <span data-ttu-id="9a345-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a345-123">Optional.</span></span> <span data-ttu-id="9a345-124">Valor booleano que indica si el comando está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9a345-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="9a345-125">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="9a345-125">The default value is **True**.</span></span> <span data-ttu-id="9a345-126">Para obtener más información, vea la propiedad [Enabled](enabled-property.md) del objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="9a345-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="9a345-127">*Visible*</span></span> | <span data-ttu-id="9a345-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a345-128">Optional.</span></span> <span data-ttu-id="9a345-129">Un valor booleano que indica si el comando está visible en el menú emergente del carácter para el carácter cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="9a345-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="9a345-130">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="9a345-130">The default value is **True**.</span></span> <span data-ttu-id="9a345-131">Para obtener más información, vea la propiedad [visible](visible-property.md) del objeto de [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a345-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a345-132">Remarks</span></span>

<span data-ttu-id="9a345-133">El valor de la propiedad [Name](name-property.md) de un objeto [Command](the-command-object.md) debe ser único dentro de su colección [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="9a345-134">Debe quitar un comando para poder crear un nuevo comando con el mismo valor de la propiedad nombre.</span><span class="sxs-lookup"><span data-stu-id="9a345-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="9a345-135">Al intentar crear un comando con una propiedad Name que ya existe, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9a345-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="9a345-136">Este método también devuelve un objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9a345-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="9a345-137">Esto permite declarar un objeto y asignarle un comando cuando se llama a addMethod.</span><span class="sxs-lookup"><span data-stu-id="9a345-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="9a345-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a345-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a345-139">**Insert (método)**</span><span class="sxs-lookup"><span data-stu-id="9a345-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="9a345-140">**método RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="9a345-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="9a345-141">**Remove (método)**</span><span class="sxs-lookup"><span data-stu-id="9a345-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




