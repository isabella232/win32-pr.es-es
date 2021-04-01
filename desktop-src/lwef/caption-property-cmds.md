---
title: Propiedad Caption (objeto de colección Commands)
description: Propiedad Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149797"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="a4896-103">Propiedad Caption (objeto de colección Commands)</span><span class="sxs-lookup"><span data-stu-id="a4896-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="a4896-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4896-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a4896-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a4896-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a4896-106">Determina el texto que se muestra para un objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="a4896-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="a4896-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a4896-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a4896-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \* [Commands. Caption](caption-property.md) ( \[  =  *cadena* )\]</span><span class="sxs-lookup"><span data-stu-id="a4896-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="a4896-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a4896-109">Part</span></span>     | <span data-ttu-id="a4896-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4896-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="a4896-111">*string*</span><span class="sxs-lookup"><span data-stu-id="a4896-111">*string*</span></span> | <span data-ttu-id="a4896-112">Expresión de cadena que se evalúa como el texto que se muestra como título.</span><span class="sxs-lookup"><span data-stu-id="a4896-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4896-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4896-113">Remarks</span></span>

<span data-ttu-id="a4896-114">Al establecer la propiedad [**Caption**](caption-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**visible**](visible-property.md) esté establecida en true y la aplicación no sea el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="a4896-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="a4896-115">Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="a4896-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="a4896-116">Si define comandos para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tiene un [**título**](caption-property.md), normalmente también se define un **título** para la colección de **comandos** asociada.</span><span class="sxs-lookup"><span data-stu-id="a4896-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
