---
title: Propiedad FontName (objeto Balloon)
description: Obtenga información sobre la propiedad de objeto FontName Balloon. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068271"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="fb330-104">Propiedad FontName (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="fb330-104">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="fb330-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb330-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fb330-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb330-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fb330-107">Devuelve o establece la fuente utilizada en el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="fb330-107">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="fb330-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="fb330-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fb330-109">*agent.\***Caracteres("**_CharacterID_*_"). Fuente Balloon.FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="fb330-109">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="fb330-110">Parte</span><span class="sxs-lookup"><span data-stu-id="fb330-110">Part</span></span>   | <span data-ttu-id="fb330-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb330-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="fb330-112">*Fuente*</span><span class="sxs-lookup"><span data-stu-id="fb330-112">*font*</span></span> | <span data-ttu-id="fb330-113">Valor de cadena correspondiente al nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="fb330-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb330-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb330-114">Remarks</span></span>

<span data-ttu-id="fb330-115">La [**propiedad FontName**](fontname-property.md) define la fuente utilizada para mostrar texto en la ventana de globo de palabras de una cadena.</span><span class="sxs-lookup"><span data-stu-id="fb330-115">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="fb330-116">El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb330-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fb330-117">Además, el usuario puede invalidar la configuración de fuente de todos los caracteres de la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb330-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="fb330-118">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="fb330-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="fb330-119">Si usa un carácter que no compiló, compruebe las propiedades [**FontName**](fontname-property.md) y [**FontCharSet**](fontcharset-property.md) del carácter para determinar si son adecuadas para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="fb330-119">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="fb330-120">Es posible que tenga que establecer estos valores antes de usar el [**método Speak**](speak-method.md) para asegurarse de que se muestra el texto adecuado en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="fb330-120">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




