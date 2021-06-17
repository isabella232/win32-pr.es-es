---
title: Propiedad Caption (objeto de colección Commands)
description: Obtenga información sobre la propiedad Caption del objeto Colección de comandos. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262058"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="85bc7-104">Propiedad Caption (objeto de colección Commands)</span><span class="sxs-lookup"><span data-stu-id="85bc7-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="85bc7-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85bc7-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="85bc7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85bc7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="85bc7-107">Determina el texto que se muestra para un [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="85bc7-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="85bc7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="85bc7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="85bc7-109">*agent\***. Caracteres ("**_CharacterID_*_")._ \* [Cadena Commands.Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="85bc7-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="85bc7-110">Parte</span><span class="sxs-lookup"><span data-stu-id="85bc7-110">Part</span></span>     | <span data-ttu-id="85bc7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="85bc7-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="85bc7-112">*string*</span><span class="sxs-lookup"><span data-stu-id="85bc7-112">*string*</span></span> | <span data-ttu-id="85bc7-113">Expresión de cadena que se evalúa como el texto mostrado como título.</span><span class="sxs-lookup"><span data-stu-id="85bc7-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85bc7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85bc7-114">Remarks</span></span>

<span data-ttu-id="85bc7-115">Al establecer la propiedad [**Caption**](caption-property.md) de la colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**Visible**](visible-property.md) esté establecida en True y la aplicación no sea el cliente activo de entrada.</span><span class="sxs-lookup"><span data-stu-id="85bc7-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="85bc7-116">Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yand (&) delante de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="85bc7-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="85bc7-117">Si define comandos para una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) que tiene un [**título**](caption-property.md), normalmente también se define un título **para** su colección **Commands** asociada.</span><span class="sxs-lookup"><span data-stu-id="85bc7-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
