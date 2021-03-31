---
title: Propiedad DefaultCommand
description: Propiedad DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077677"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="af3f2-103">Propiedad DefaultCommand</span><span class="sxs-lookup"><span data-stu-id="af3f2-103">DefaultCommand Property</span></span>

<span data-ttu-id="af3f2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af3f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af3f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="af3f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af3f2-106">Devuelve o establece el comando predeterminado del objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="af3f2-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="af3f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="af3f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="af3f2-108">Caracteres del agente \*. \* \* \*\* \*  **("***CharacterID***"). Commands. DefaultCommand** ( \[  =  *cadena* )\]</span><span class="sxs-lookup"><span data-stu-id="af3f2-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="af3f2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="af3f2-109">Part</span></span>     | <span data-ttu-id="af3f2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af3f2-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af3f2-111">*string*</span><span class="sxs-lookup"><span data-stu-id="af3f2-111">*string*</span></span> | <span data-ttu-id="af3f2-112">Un valor de cadena que identifica el nombre (ID.) del [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="af3f2-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af3f2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af3f2-113">Remarks</span></span>

<span data-ttu-id="af3f2-114">Esta propiedad permite establecer un [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) como el comando predeterminado, para representarlo en negrita.</span><span class="sxs-lookup"><span data-stu-id="af3f2-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="af3f2-115">Esto no cambia realmente el control de comandos ni los eventos de doble clic.</span><span class="sxs-lookup"><span data-stu-id="af3f2-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="af3f2-116">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="af3f2-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 