---
description: Implementado por el shell para ayudar a los programadores de script y Microsoft Visual Basic a usar algunas de las características disponibles en el shell. El objeto ShellUIHelper no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.
title: Objeto ShellUIHelper (exdisp. h)
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
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986019"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="13682-105">Objeto ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="13682-105">ShellUIHelper object</span></span>

<span data-ttu-id="13682-106">Implementado por el shell para ayudar a los programadores de script y Microsoft Visual Basic a usar algunas de las características disponibles en el shell.</span><span class="sxs-lookup"><span data-stu-id="13682-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="13682-107">El objeto **ShellUIHelper** no tiene propiedades ni eventos.</span><span class="sxs-lookup"><span data-stu-id="13682-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="13682-108">Se proporcionan métodos para agregar elementos al shell.</span><span class="sxs-lookup"><span data-stu-id="13682-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="13682-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="13682-109">Members</span></span>

<span data-ttu-id="13682-110">El objeto **ShellUIHelper** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13682-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="13682-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="13682-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13682-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="13682-112">Methods</span></span>

<span data-ttu-id="13682-113">El objeto **ShellUIHelper** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="13682-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="13682-114">Método</span><span class="sxs-lookup"><span data-stu-id="13682-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="13682-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="13682-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13682-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="13682-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13682-117">Agrega un nuevo canal a la lista de canales en el menú <strong>Favoritos</strong> de Internet Explorer y en la barra de <strong>canales</strong> del escritorio.</span><span class="sxs-lookup"><span data-stu-id="13682-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="13682-118">Este método ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13682-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="13682-119">En ese sistema operativo, devuelve E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="13682-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="13682-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="13682-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13682-121">Agrega un elemento al escritorio activo.</span><span class="sxs-lookup"><span data-stu-id="13682-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13682-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="13682-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13682-123">Muestra la interfaz de usuario predeterminada para crear un elemento favorito.</span><span class="sxs-lookup"><span data-stu-id="13682-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="13682-124">La interfaz de usuario se inicializa con los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="13682-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="13682-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="13682-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13682-126">Indica si se ha suscrito a una dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="13682-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="13682-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13682-127">Requirements</span></span>



| <span data-ttu-id="13682-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="13682-128">Requirement</span></span> | <span data-ttu-id="13682-129">Value</span><span class="sxs-lookup"><span data-stu-id="13682-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13682-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13682-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13682-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="13682-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="13682-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13682-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13682-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13682-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13682-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13682-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="13682-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13682-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="13682-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13682-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13682-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="13682-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




