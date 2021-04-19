---
title: Método play (características heredadas del entorno de Windows)
description: Play (método)
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695816"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="083dd-103">Método play (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="083dd-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="083dd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="083dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="083dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="083dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="083dd-106">Reproduce la animación especificada para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="083dd-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="083dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="083dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="083dd-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Reproducir_* "*AnimationName*"</span><span class="sxs-lookup"><span data-stu-id="083dd-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="083dd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="083dd-109">Part</span></span>            | <span data-ttu-id="083dd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="083dd-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="083dd-111">*AnimationName*</span><span class="sxs-lookup"><span data-stu-id="083dd-111">*AnimationName*</span></span> | <span data-ttu-id="083dd-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="083dd-112">Required.</span></span> <span data-ttu-id="083dd-113">Cadena que especifica el nombre de una secuencia de animación.</span><span class="sxs-lookup"><span data-stu-id="083dd-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="083dd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="083dd-114">Remarks</span></span>

<span data-ttu-id="083dd-115">El nombre de una animación se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="083dd-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="083dd-116">Antes de reproducir la animación especificada, el servidor intenta reproducir la animación de **retorno** de la animación anterior, si se ha asignado una.</span><span class="sxs-lookup"><span data-stu-id="083dd-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="083dd-117">Al tener acceso a las animaciones de un carácter mediante un protocolo de archivo convencional, puede simplemente usar el método **Play** especificando el nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="083dd-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="083dd-118">Sin embargo, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método **Get** para cargar la animación antes de llamar al método **Play** .</span><span class="sxs-lookup"><span data-stu-id="083dd-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="083dd-119">Para obtener más información, vea el método **Get** .</span><span class="sxs-lookup"><span data-stu-id="083dd-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="083dd-120">Para simplificar la sintaxis, puede declarar una referencia de objeto y establecerla para que haga referencia al objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) y use la referencia como parte de las instrucciones de **reproducción** :</span><span class="sxs-lookup"><span data-stu-id="083dd-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="083dd-121">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="083dd-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="083dd-122">Además, si especifica una animación que no está cargada o si el carácter no se ha cargado correctamente, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="083dd-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="083dd-123">Sin embargo, si la animación no existe y los datos del carácter ya se han cargado correctamente, el servidor genera un error.</span><span class="sxs-lookup"><span data-stu-id="083dd-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="083dd-124">El método **Play** no hace que el carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="083dd-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="083dd-125">Si el carácter no está visible, el servidor reproduce la animación de manera invisible y establece la propiedad [**status**](status-property.md) del objeto [**request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="083dd-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
