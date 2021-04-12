---
title: Propiedad FontCharSet
description: Propiedad FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357591"
---
# <a name="fontcharset-property"></a><span data-ttu-id="f20b0-103">Propiedad FontCharSet</span><span class="sxs-lookup"><span data-stu-id="f20b0-103">FontCharSet Property</span></span>

<span data-ttu-id="f20b0-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f20b0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f20b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="f20b0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f20b0-106">Devuelve o establece el juego de caracteres de la fuente que se muestra en el globo de palabras del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="f20b0-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="f20b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="f20b0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f20b0-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Balloon. FontCharSet* \*  \[  =  *valor*\]</span><span class="sxs-lookup"><span data-stu-id="f20b0-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="f20b0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f20b0-109">Part</span></span>    | <span data-ttu-id="f20b0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f20b0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f20b0-111">*value*</span><span class="sxs-lookup"><span data-stu-id="f20b0-111">*value*</span></span> | <span data-ttu-id="f20b0-112">Valor entero que especifica el juego de caracteres utilizado por la fuente.</span><span class="sxs-lookup"><span data-stu-id="f20b0-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="f20b0-113">A continuación se muestran algunos valores de configuración comunes para el valor: 0 caracteres estándar de Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f20b0-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="f20b0-114">1 juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f20b0-114">1 Default character set.</span></span><br/> <span data-ttu-id="f20b0-115">2 el juego de caracteres de símbolos.</span><span class="sxs-lookup"><span data-stu-id="f20b0-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="f20b0-116">128 juego de caracteres de doble byte (DBCS) único para la versión en japonés de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20b0-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="f20b0-117">129 juego de caracteres de doble byte (DBCS) único para la versión coreana de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20b0-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="f20b0-118">134 juego de caracteres de doble byte (DBCS) único para la versión de chino simplificado de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20b0-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="f20b0-119">136 juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20b0-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="f20b0-120">255 caracteres extendidos que se muestran normalmente en aplicaciones de Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="f20b0-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="f20b0-121">Para otros valores de juego de caracteres, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="f20b0-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f20b0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f20b0-122">Remarks</span></span>

<span data-ttu-id="f20b0-123">El valor predeterminado para el juego de caracteres del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f20b0-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f20b0-124">Además, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f20b0-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="f20b0-125">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f20b0-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="f20b0-126">Si usa un carácter que no ha compilado, compruebe las propiedades [**FontName**](fontname-property.md) y **FontCharSet** del carácter para determinar si son adecuados para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="f20b0-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="f20b0-127">Es posible que tenga que establecer estos valores antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="f20b0-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f20b0-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f20b0-128">See Also</span></span>

[<span data-ttu-id="f20b0-129">**FontName (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="f20b0-129">**FontName property**</span></span>](fontname-property.md)


 

 





