---
description: Implementado por shell para ayudar a crear scripts y microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El objeto ShellUIHelper no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.
title: Objeto ShellUIHelper (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842436"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="5843a-105">Objeto ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="5843a-105">ShellUIHelper object</span></span>

<span data-ttu-id="5843a-106">Implementado por shell para ayudar a crear scripts y microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell.</span><span class="sxs-lookup"><span data-stu-id="5843a-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="5843a-107">El **objeto ShellUIHelper** no tiene propiedades ni eventos.</span><span class="sxs-lookup"><span data-stu-id="5843a-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="5843a-108">Se proporcionan métodos para agregar elementos al shell.</span><span class="sxs-lookup"><span data-stu-id="5843a-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="5843a-109">Members</span><span class="sxs-lookup"><span data-stu-id="5843a-109">Members</span></span>

<span data-ttu-id="5843a-110">El **objeto ShellUIHelper** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5843a-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="5843a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5843a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5843a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5843a-112">Methods</span></span>

<span data-ttu-id="5843a-113">El **objeto ShellUIHelper** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5843a-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="5843a-114">Método</span><span class="sxs-lookup"><span data-stu-id="5843a-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5843a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5843a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="5843a-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="5843a-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="5843a-117">Agrega un nuevo canal a la lista de <strong>canales</strong> del menú Internet Explorer Favoritos y a la barra <strong>Canal</strong> del escritorio.</span><span class="sxs-lookup"><span data-stu-id="5843a-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5843a-118">Este método ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5843a-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="5843a-119">En ese sistema operativo, devuelve E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5843a-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="5843a-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="5843a-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="5843a-121">Agrega un elemento al Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="5843a-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="5843a-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="5843a-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="5843a-123">Muestra la interfaz de usuario predeterminada para crear un elemento favorito.</span><span class="sxs-lookup"><span data-stu-id="5843a-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="5843a-124">La interfaz de usuario se inicializa en los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="5843a-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="5843a-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="5843a-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="5843a-126">Indica si se ha suscrito una dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="5843a-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5843a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5843a-127">Requirements</span></span>



| <span data-ttu-id="5843a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5843a-128">Requirement</span></span> | <span data-ttu-id="5843a-129">Value</span><span class="sxs-lookup"><span data-stu-id="5843a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5843a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5843a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5843a-131">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="5843a-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5843a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5843a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5843a-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5843a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5843a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5843a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5843a-135"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5843a-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="5843a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5843a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5843a-137"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5843a-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




