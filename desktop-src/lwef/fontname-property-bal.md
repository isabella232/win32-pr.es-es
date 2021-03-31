---
title: FontName (propiedad, objeto Balloon)
description: FontName (propiedad)
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149820"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="690a0-103">FontName (propiedad, objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="690a0-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="690a0-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="690a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="690a0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="690a0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="690a0-106">Devuelve o establece la fuente utilizada en el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="690a0-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="690a0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="690a0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="690a0-108">\*Caracteres Agent. \***("**_CharacterID_\*_"). Fuente Balloon. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="690a0-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="690a0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="690a0-109">Part</span></span>   | <span data-ttu-id="690a0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="690a0-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="690a0-111">*tipo*</span><span class="sxs-lookup"><span data-stu-id="690a0-111">*font*</span></span> | <span data-ttu-id="690a0-112">Valor de cadena que corresponde al nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="690a0-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="690a0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="690a0-113">Remarks</span></span>

<span data-ttu-id="690a0-114">La propiedad [**FontName**](fontname-property.md) define la fuente utilizada para mostrar texto en la ventana de globo de palabras de una cadena.</span><span class="sxs-lookup"><span data-stu-id="690a0-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="690a0-115">El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="690a0-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="690a0-116">Además, el usuario puede invalidar la configuración de fuente para todos los caracteres de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="690a0-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="690a0-117">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="690a0-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="690a0-118">Si usa un carácter que no ha compilado, compruebe las propiedades [**FontName**](fontname-property.md) y [**FontCharSet**](fontcharset-property.md) del carácter para determinar si son adecuados para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="690a0-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="690a0-119">Es posible que tenga que establecer estos valores antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="690a0-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




