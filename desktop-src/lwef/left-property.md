---
title: Left (propiedad, Characters, objeto)
description: Left (propiedad)
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105665911"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="16af8-103">Left (propiedad, Characters, objeto)</span><span class="sxs-lookup"><span data-stu-id="16af8-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="16af8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16af8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="16af8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="16af8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="16af8-106">Devuelve o establece el borde izquierdo del marco del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="16af8-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="16af8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="16af8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="16af8-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \*  \[  =  *Valor* izquierdo\]</span><span class="sxs-lookup"><span data-stu-id="16af8-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="16af8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="16af8-109">Part</span></span>    | <span data-ttu-id="16af8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="16af8-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="16af8-111">*value*</span><span class="sxs-lookup"><span data-stu-id="16af8-111">*value*</span></span> | <span data-ttu-id="16af8-112">Entero largo que especifica el borde izquierdo del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="16af8-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16af8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16af8-113">Remarks</span></span>

<span data-ttu-id="16af8-114">La propiedad **left** siempre se expresa en píxeles, en relación con el origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="16af8-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="16af8-115">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="16af8-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="16af8-116">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="16af8-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




