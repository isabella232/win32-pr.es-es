---
title: El objeto Command
description: El objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714369"
---
# <a name="the-command-object"></a><span data-ttu-id="a85a8-103">El objeto Command</span><span class="sxs-lookup"><span data-stu-id="a85a8-103">The Command Object</span></span>

<span data-ttu-id="a85a8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a85a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a85a8-105">Un objeto [**Command**](/windows/desktop/lwef/the-command-object) es un elemento de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="a85a8-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="a85a8-106">El servidor proporciona al usuario acceso a los objetos de **comando** cuando la aplicación cliente pasa a ser de entrada activa.</span><span class="sxs-lookup"><span data-stu-id="a85a8-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="a85a8-107">Propiedades del objeto de comando</span><span class="sxs-lookup"><span data-stu-id="a85a8-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="a85a8-108">Para tener acceso a la propiedad de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) , se hace referencia a él en su colección mediante su propiedad [**Name**](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a85a8-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="a85a8-109">En VBScript y Visual Basic puede usar la propiedad **nombre** directamente:</span><span class="sxs-lookup"><span data-stu-id="a85a8-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="a85a8-110">Para los lenguajes de programación que no admiten colecciones, use el método de [**comando**](command-method.md) :</span><span class="sxs-lookup"><span data-stu-id="a85a8-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="a85a8-111">También puede hacer referencia a un objeto de comando mediante la creación de una referencia a él.</span><span class="sxs-lookup"><span data-stu-id="a85a8-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="a85a8-112">En Visual Basic, declare una variable de objeto y use la instrucción SET para crear la referencia:</span><span class="sxs-lookup"><span data-stu-id="a85a8-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="a85a8-113">En Visual Basic 5,0, también puede declarar el objeto como de tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) y crear la referencia.</span><span class="sxs-lookup"><span data-stu-id="a85a8-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="a85a8-114">Esta Convención permite el enlace anticipado, lo que da como resultado un mejor rendimiento:</span><span class="sxs-lookup"><span data-stu-id="a85a8-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="a85a8-115">En VBScript, puede declarar una referencia como un tipo determinado, pero todavía puede declarar la variable y establecerla en el [**comando**](/windows/desktop/lwef/the-command-object) de la colección:</span><span class="sxs-lookup"><span data-stu-id="a85a8-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="a85a8-116">Puede aparecer un comando en el menú emergente del carácter y en la ventana comandos, o bien en ambos.</span><span class="sxs-lookup"><span data-stu-id="a85a8-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="a85a8-117">Para que aparezca en el menú emergente, debe tener un título y tener la propiedad [**visible**](visible-property.md) establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="a85a8-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="a85a8-118">Además, la propiedad **visible** del objeto de colección Commands también debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="a85a8-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="a85a8-119">Para que aparezca en la ventana comandos, un [**comando**](/windows/desktop/lwef/the-command-object) debe tener establecidas las propiedades [**Caption**](caption-property.md) y [**Voice**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a85a8-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="a85a8-120">Tenga en cuenta que las entradas del menú emergente de un carácter no cambian mientras se muestra el menú.</span><span class="sxs-lookup"><span data-stu-id="a85a8-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="a85a8-121">Si agrega o quita comandos o cambia sus propiedades mientras se muestra el menú emergente del carácter, el menú muestra esos cambios cada vez que el usuario lo muestra.</span><span class="sxs-lookup"><span data-stu-id="a85a8-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="a85a8-122">Sin embargo, la ventana comandos refleja dinámicamente los cambios que realice.</span><span class="sxs-lookup"><span data-stu-id="a85a8-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="a85a8-123">En la tabla siguiente se resume el modo en que las propiedades de un [**comando**](/windows/desktop/lwef/the-command-object) afectan a su presentación:</span><span class="sxs-lookup"><span data-stu-id="a85a8-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="a85a8-124">Propiedad Caption</span><span class="sxs-lookup"><span data-stu-id="a85a8-124">Caption Property</span></span>

<span data-ttu-id="a85a8-125">Propiedad Voice-Caption</span><span class="sxs-lookup"><span data-stu-id="a85a8-125">Voice-Caption Property</span></span>

<span data-ttu-id="a85a8-126">Propiedad Voice</span><span class="sxs-lookup"><span data-stu-id="a85a8-126">Voice Property</span></span>

<span data-ttu-id="a85a8-127">Propiedad visible</span><span class="sxs-lookup"><span data-stu-id="a85a8-127">Visible Property</span></span>

<span data-ttu-id="a85a8-128">Propiedad Enabled</span><span class="sxs-lookup"><span data-stu-id="a85a8-128">Enabled Property</span></span>

<span data-ttu-id="a85a8-129">Aparece en el menú emergente del carácter</span><span class="sxs-lookup"><span data-stu-id="a85a8-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="a85a8-130">Aparece en la ventana comandos</span><span class="sxs-lookup"><span data-stu-id="a85a8-130">Appears in Commands Window</span></span>

<span data-ttu-id="a85a8-131">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-131">Yes</span></span>

<span data-ttu-id="a85a8-132">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-132">Yes</span></span>

<span data-ttu-id="a85a8-133">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-133">Yes</span></span>

<span data-ttu-id="a85a8-134">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-134">True</span></span>

<span data-ttu-id="a85a8-135">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-135">True</span></span>

<span data-ttu-id="a85a8-136">Normal, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-137">Sí, uso de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="a85a8-138">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-138">Yes</span></span>

<span data-ttu-id="a85a8-139">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-139">Yes</span></span>

<span data-ttu-id="a85a8-140">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-140">Yes</span></span>

<span data-ttu-id="a85a8-141">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-141">True</span></span>

<span data-ttu-id="a85a8-142">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-142">False</span></span>

<span data-ttu-id="a85a8-143">Deshabilitado, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-144">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-144">No</span></span>

<span data-ttu-id="a85a8-145">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-145">Yes</span></span>

<span data-ttu-id="a85a8-146">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-146">Yes</span></span>

<span data-ttu-id="a85a8-147">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-147">Yes</span></span>

<span data-ttu-id="a85a8-148">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-148">False</span></span>

<span data-ttu-id="a85a8-149">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-149">True</span></span>

<span data-ttu-id="a85a8-150">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-150">Does not appear</span></span>

<span data-ttu-id="a85a8-151">Sí, uso de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="a85a8-152">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-152">Yes</span></span>

<span data-ttu-id="a85a8-153">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-153">Yes</span></span>

<span data-ttu-id="a85a8-154">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-154">Yes</span></span>

<span data-ttu-id="a85a8-155">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-155">False</span></span>

<span data-ttu-id="a85a8-156">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-156">False</span></span>

<span data-ttu-id="a85a8-157">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-157">Does not appear</span></span>

<span data-ttu-id="a85a8-158">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-158">No</span></span>

<span data-ttu-id="a85a8-159">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-159">Yes</span></span>

<span data-ttu-id="a85a8-160">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-160">Yes</span></span>

<span data-ttu-id="a85a8-161">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-161">No</span></span> 

<span data-ttu-id="a85a8-162">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-162">True</span></span>

<span data-ttu-id="a85a8-163">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-163">True</span></span>

<span data-ttu-id="a85a8-164">Normal, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-165">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-165">No</span></span>

<span data-ttu-id="a85a8-166">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-166">Yes</span></span>

<span data-ttu-id="a85a8-167">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-167">Yes</span></span>

<span data-ttu-id="a85a8-168">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-168">No</span></span> 

<span data-ttu-id="a85a8-169">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-169">True</span></span>

<span data-ttu-id="a85a8-170">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-170">False</span></span>

<span data-ttu-id="a85a8-171">Deshabilitado, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-172">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-172">No</span></span>

<span data-ttu-id="a85a8-173">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-173">Yes</span></span>

<span data-ttu-id="a85a8-174">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-174">Yes</span></span>

<span data-ttu-id="a85a8-175">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-175">No</span></span> 

<span data-ttu-id="a85a8-176">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-176">False</span></span>

<span data-ttu-id="a85a8-177">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-177">True</span></span>

<span data-ttu-id="a85a8-178">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-178">Does not appear</span></span>

<span data-ttu-id="a85a8-179">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-179">No</span></span>

<span data-ttu-id="a85a8-180">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-180">Yes</span></span>

<span data-ttu-id="a85a8-181">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-181">Yes</span></span>

<span data-ttu-id="a85a8-182">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-182">No</span></span> 

<span data-ttu-id="a85a8-183">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-183">False</span></span>

<span data-ttu-id="a85a8-184">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-184">False</span></span>

<span data-ttu-id="a85a8-185">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-185">Does not appear</span></span>

<span data-ttu-id="a85a8-186">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-186">No</span></span>

<span data-ttu-id="a85a8-187">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-187">No</span></span> 

<span data-ttu-id="a85a8-188">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-188">Yes</span></span>

<span data-ttu-id="a85a8-189">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-189">Yes</span></span>

<span data-ttu-id="a85a8-190">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-190">True</span></span>

<span data-ttu-id="a85a8-191">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-191">True</span></span>

<span data-ttu-id="a85a8-192">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-192">Does not appear</span></span>

<span data-ttu-id="a85a8-193">Sí, uso de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="a85a8-194">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-194">No</span></span> 

<span data-ttu-id="a85a8-195">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-195">Yes</span></span>

<span data-ttu-id="a85a8-196">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-196">Yes</span></span>

<span data-ttu-id="a85a8-197">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-197">True</span></span>

<span data-ttu-id="a85a8-198">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-198">False</span></span>

<span data-ttu-id="a85a8-199">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-199">Does not appear</span></span>

<span data-ttu-id="a85a8-200">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-200">No</span></span>

<span data-ttu-id="a85a8-201">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-201">No</span></span> 

<span data-ttu-id="a85a8-202">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-202">Yes</span></span>

<span data-ttu-id="a85a8-203">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-203">Yes</span></span>

<span data-ttu-id="a85a8-204">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-204">False</span></span>

<span data-ttu-id="a85a8-205">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-205">True</span></span>

<span data-ttu-id="a85a8-206">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-206">Does not appear</span></span>

<span data-ttu-id="a85a8-207">Sí, uso de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="a85a8-208">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-208">No</span></span> 

<span data-ttu-id="a85a8-209">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-209">Yes</span></span>

<span data-ttu-id="a85a8-210">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-210">Yes</span></span>

<span data-ttu-id="a85a8-211">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-211">False</span></span>

<span data-ttu-id="a85a8-212">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-212">False</span></span>

<span data-ttu-id="a85a8-213">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-213">Does not appear</span></span>

<span data-ttu-id="a85a8-214">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-214">No</span></span>

<span data-ttu-id="a85a8-215">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-215">No</span></span> 

<span data-ttu-id="a85a8-216">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-216">Yes</span></span>

<span data-ttu-id="a85a8-217">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-217">No</span></span> 

<span data-ttu-id="a85a8-218">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-218">True</span></span>

<span data-ttu-id="a85a8-219">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-219">True</span></span>

<span data-ttu-id="a85a8-220">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-220">Does not appear</span></span>

<span data-ttu-id="a85a8-221">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-221">No</span></span>

<span data-ttu-id="a85a8-222">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-222">No</span></span> 

<span data-ttu-id="a85a8-223">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-223">Yes</span></span>

<span data-ttu-id="a85a8-224">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-224">No</span></span> 

<span data-ttu-id="a85a8-225">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-225">True</span></span>

<span data-ttu-id="a85a8-226">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-226">False</span></span>

<span data-ttu-id="a85a8-227">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-227">Does not appear</span></span>

<span data-ttu-id="a85a8-228">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-228">No</span></span>

<span data-ttu-id="a85a8-229">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-229">No</span></span> 

<span data-ttu-id="a85a8-230">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-230">Yes</span></span>

<span data-ttu-id="a85a8-231">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-231">No</span></span> 

<span data-ttu-id="a85a8-232">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-232">False</span></span>

<span data-ttu-id="a85a8-233">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-233">True</span></span>

<span data-ttu-id="a85a8-234">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-234">Does not appear</span></span>

<span data-ttu-id="a85a8-235">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-235">No</span></span>

<span data-ttu-id="a85a8-236">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-236">No</span></span> 

<span data-ttu-id="a85a8-237">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-237">Yes</span></span>

<span data-ttu-id="a85a8-238">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-238">No</span></span> 

<span data-ttu-id="a85a8-239">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-239">False</span></span>

<span data-ttu-id="a85a8-240">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-240">False</span></span>

<span data-ttu-id="a85a8-241">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-241">Does not appear</span></span>

<span data-ttu-id="a85a8-242">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-242">No</span></span>

<span data-ttu-id="a85a8-243">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-243">Yes</span></span>

<span data-ttu-id="a85a8-244">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-244">No</span></span> 

<span data-ttu-id="a85a8-245">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-245">Yes</span></span>

<span data-ttu-id="a85a8-246">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-246">True</span></span>

<span data-ttu-id="a85a8-247">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-247">True</span></span>

<span data-ttu-id="a85a8-248">Normal, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-249">Sí, usar [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-250">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-250">Yes</span></span>

<span data-ttu-id="a85a8-251">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-251">No</span></span> 

<span data-ttu-id="a85a8-252">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-252">Yes</span></span>

<span data-ttu-id="a85a8-253">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-253">True</span></span>

<span data-ttu-id="a85a8-254">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-254">False</span></span>

<span data-ttu-id="a85a8-255">Deshabilitado, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-256">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-256">No</span></span>

<span data-ttu-id="a85a8-257">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-257">Yes</span></span>

<span data-ttu-id="a85a8-258">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-258">No</span></span> 

<span data-ttu-id="a85a8-259">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-259">Yes</span></span>

<span data-ttu-id="a85a8-260">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-260">False</span></span>

<span data-ttu-id="a85a8-261">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-261">True</span></span>

<span data-ttu-id="a85a8-262">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-262">Does not appear</span></span>

<span data-ttu-id="a85a8-263">Sí, usar [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-264">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-264">Yes</span></span>

<span data-ttu-id="a85a8-265">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-265">No</span></span> 

<span data-ttu-id="a85a8-266">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-266">Yes</span></span>

<span data-ttu-id="a85a8-267">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-267">False</span></span>

<span data-ttu-id="a85a8-268">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-268">False</span></span>

<span data-ttu-id="a85a8-269">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-269">Does not appear</span></span>

<span data-ttu-id="a85a8-270">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-270">No</span></span>

<span data-ttu-id="a85a8-271">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-271">Yes</span></span>

<span data-ttu-id="a85a8-272">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-272">No</span></span> 

<span data-ttu-id="a85a8-273">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-273">No</span></span> 

<span data-ttu-id="a85a8-274">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-274">True</span></span>

<span data-ttu-id="a85a8-275">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-275">True</span></span>

<span data-ttu-id="a85a8-276">Normal, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-277">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-277">No</span></span>

<span data-ttu-id="a85a8-278">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-278">Yes</span></span>

<span data-ttu-id="a85a8-279">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-279">No</span></span> 

<span data-ttu-id="a85a8-280">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-280">No</span></span> 

<span data-ttu-id="a85a8-281">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-281">True</span></span>

<span data-ttu-id="a85a8-282">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-282">False</span></span>

<span data-ttu-id="a85a8-283">Deshabilitado, con [ **título**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a85a8-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="a85a8-284">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-284">No</span></span>

<span data-ttu-id="a85a8-285">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-285">Yes</span></span>

<span data-ttu-id="a85a8-286">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-286">No</span></span> 

<span data-ttu-id="a85a8-287">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-287">No</span></span> 

<span data-ttu-id="a85a8-288">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-288">False</span></span>

<span data-ttu-id="a85a8-289">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-289">True</span></span>

<span data-ttu-id="a85a8-290">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-290">Does not appear</span></span>

<span data-ttu-id="a85a8-291">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-291">No</span></span>

<span data-ttu-id="a85a8-292">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-292">Yes</span></span>

<span data-ttu-id="a85a8-293">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-293">No</span></span> 

<span data-ttu-id="a85a8-294">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-294">No</span></span> 

<span data-ttu-id="a85a8-295">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-295">False</span></span>

<span data-ttu-id="a85a8-296">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-296">False</span></span>

<span data-ttu-id="a85a8-297">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-297">Does not appear</span></span>

<span data-ttu-id="a85a8-298">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-298">No</span></span>

<span data-ttu-id="a85a8-299">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-299">No</span></span> 

<span data-ttu-id="a85a8-300">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-300">No</span></span> 

<span data-ttu-id="a85a8-301">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-301">Yes</span></span>

<span data-ttu-id="a85a8-302">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-302">True</span></span>

<span data-ttu-id="a85a8-303">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-303">True</span></span>

<span data-ttu-id="a85a8-304">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-304">Does not appear</span></span>

<span data-ttu-id="a85a8-305">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-305">No</span></span> 

<span data-ttu-id="a85a8-306">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-306">No</span></span> 

<span data-ttu-id="a85a8-307">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-307">No</span></span> 

<span data-ttu-id="a85a8-308">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-308">Yes</span></span>

<span data-ttu-id="a85a8-309">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-309">True</span></span>

<span data-ttu-id="a85a8-310">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-310">False</span></span>

<span data-ttu-id="a85a8-311">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-311">Does not appear</span></span>

<span data-ttu-id="a85a8-312">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-312">No</span></span>

<span data-ttu-id="a85a8-313">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-313">No</span></span> 

<span data-ttu-id="a85a8-314">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-314">No</span></span> 

<span data-ttu-id="a85a8-315">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-315">Yes</span></span>

<span data-ttu-id="a85a8-316">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-316">False</span></span>

<span data-ttu-id="a85a8-317">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-317">True</span></span>

<span data-ttu-id="a85a8-318">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-318">Does not appear</span></span>

<span data-ttu-id="a85a8-319">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-319">No</span></span> 

<span data-ttu-id="a85a8-320">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-320">No</span></span> 

<span data-ttu-id="a85a8-321">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-321">No</span></span> 

<span data-ttu-id="a85a8-322">Sí</span><span class="sxs-lookup"><span data-stu-id="a85a8-322">Yes</span></span>

<span data-ttu-id="a85a8-323">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-323">False</span></span>

<span data-ttu-id="a85a8-324">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-324">False</span></span>

<span data-ttu-id="a85a8-325">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-325">Does not appear</span></span>

<span data-ttu-id="a85a8-326">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-326">No</span></span>

<span data-ttu-id="a85a8-327">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-327">No</span></span> 

<span data-ttu-id="a85a8-328">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-328">No</span></span> 

<span data-ttu-id="a85a8-329">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-329">No</span></span> 

<span data-ttu-id="a85a8-330">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-330">True</span></span>

<span data-ttu-id="a85a8-331">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-331">True</span></span>

<span data-ttu-id="a85a8-332">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-332">Does not appear</span></span>

<span data-ttu-id="a85a8-333">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-333">No</span></span>

<span data-ttu-id="a85a8-334">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-334">No</span></span> 

<span data-ttu-id="a85a8-335">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-335">No</span></span> 

<span data-ttu-id="a85a8-336">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-336">No</span></span> 

<span data-ttu-id="a85a8-337">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-337">True</span></span>

<span data-ttu-id="a85a8-338">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-338">False</span></span>

<span data-ttu-id="a85a8-339">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-339">Does not appear</span></span>

<span data-ttu-id="a85a8-340">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-340">No</span></span>

<span data-ttu-id="a85a8-341">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-341">No</span></span> 

<span data-ttu-id="a85a8-342">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-342">No</span></span> 

<span data-ttu-id="a85a8-343">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-343">No</span></span> 

<span data-ttu-id="a85a8-344">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-344">False</span></span>

<span data-ttu-id="a85a8-345">True</span><span class="sxs-lookup"><span data-stu-id="a85a8-345">True</span></span>

<span data-ttu-id="a85a8-346">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-346">Does not appear</span></span>

<span data-ttu-id="a85a8-347">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-347">No</span></span>

<span data-ttu-id="a85a8-348">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-348">No</span></span> 

<span data-ttu-id="a85a8-349">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-349">No</span></span> 

<span data-ttu-id="a85a8-350">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-350">No</span></span> 

<span data-ttu-id="a85a8-351">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-351">False</span></span>

<span data-ttu-id="a85a8-352">False</span><span class="sxs-lookup"><span data-stu-id="a85a8-352">False</span></span>

<span data-ttu-id="a85a8-353">No aparece</span><span class="sxs-lookup"><span data-stu-id="a85a8-353">Does not appear</span></span>

<span data-ttu-id="a85a8-354">No</span><span class="sxs-lookup"><span data-stu-id="a85a8-354">No</span></span>

 <span data-ttu-id="a85a8-355">Si el valor de la propiedad es NULL.</span><span class="sxs-lookup"><span data-stu-id="a85a8-355">If the property setting is null.</span></span> <span data-ttu-id="a85a8-356">En algunos lenguajes de programación, una cadena vacía no puede interpretarse igual que una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="a85a8-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="a85a8-357">El comando sigue siendo accesible mediante voz.</span><span class="sxs-lookup"><span data-stu-id="a85a8-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="a85a8-358">Cuando el servidor recibe la entrada para uno de los comandos, envía un evento de [**comando**](/windows/desktop/lwef/the-command-object) y devuelve el nombre del **comando** como un atributo del objeto [**UserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="a85a8-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="a85a8-359">Después, puede usar las instrucciones condicionales para buscar coincidencias y procesar el **comando**.</span><span class="sxs-lookup"><span data-stu-id="a85a8-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

