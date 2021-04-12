---
description: DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recursos compartidos, o enumerar recursos compartidos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Administrar recursos compartidos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104361789"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="8227a-103">Administrar recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-103">Managing DDE Shares</span></span>

<span data-ttu-id="8227a-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="8227a-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="8227a-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="8227a-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="8227a-106">DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recursos compartidos, o enumerar recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="8227a-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8227a-107">Tarea</span><span class="sxs-lookup"><span data-stu-id="8227a-107">Task</span></span></th>
<th><span data-ttu-id="8227a-108">Procedimiento</span><span class="sxs-lookup"><span data-stu-id="8227a-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8227a-109">Eliminar un recurso compartido DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="8227a-110">Utilice la función <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8227a-111">Obtener información de recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="8227a-112">Utilice la función <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8227a-113">Establecer información de recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="8227a-114">Utilice la función <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8227a-115">Enumerar recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="8227a-116">Utilice la función <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="8227a-117">También puede enumerar los recursos compartidos DDE de confianza mediante la función <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8227a-118">Enumerar usuarios conectados</span><span class="sxs-lookup"><span data-stu-id="8227a-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="8227a-119">Utilice la función <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8227a-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8227a-120">Cambiar el nombre del recurso compartido DDE</span><span class="sxs-lookup"><span data-stu-id="8227a-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="8227a-121">Elimine el recurso compartido anterior y cree un nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="8227a-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="8227a-122">Recupere la información del recurso compartido mediante <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8227a-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="8227a-123">Quite el recurso compartido mediante <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8227a-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="8227a-124">Cambie el miembro <strong>lpszShareName</strong> de la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> devuelta por <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8227a-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="8227a-125">Pase la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificada a <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8227a-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

