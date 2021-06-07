---
description: El Registro es una base de datos jerárquica que contiene datos que son críticos para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estructura del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386674"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="a276c-103">Estructura del Registro</span><span class="sxs-lookup"><span data-stu-id="a276c-103">Structure of the Registry</span></span>

<span data-ttu-id="a276c-104">El Registro es una base de datos jerárquica que contiene datos que son críticos para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows.</span><span class="sxs-lookup"><span data-stu-id="a276c-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="a276c-105">Los datos se estructuran en un formato de árbol.</span><span class="sxs-lookup"><span data-stu-id="a276c-105">The data is structured in a tree format.</span></span> <span data-ttu-id="a276c-106">Cada nodo del árbol se denomina *clave*.</span><span class="sxs-lookup"><span data-stu-id="a276c-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="a276c-107">Cada clave puede contener *subclaves* y entradas de datos *denominadas valores*.</span><span class="sxs-lookup"><span data-stu-id="a276c-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="a276c-108">A veces, la presencia de una clave son todos los datos que requiere una aplicación; otras veces, una aplicación abre una clave y usa los valores asociados a la clave.</span><span class="sxs-lookup"><span data-stu-id="a276c-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="a276c-109">Una clave puede tener cualquier número de valores y los valores pueden tener cualquier formato.</span><span class="sxs-lookup"><span data-stu-id="a276c-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="a276c-110">Para obtener más información, vea [Tipos de valor del Registro y](registry-value-types.md) [Límites de tamaño de elemento del Registro.](registry-element-size-limits.md)</span><span class="sxs-lookup"><span data-stu-id="a276c-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="a276c-111">Cada clave tiene un nombre que consta de uno o varios caracteres imprimibles.</span><span class="sxs-lookup"><span data-stu-id="a276c-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="a276c-112">Los nombres de clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a276c-112">Key names are not case sensitive.</span></span> <span data-ttu-id="a276c-113">Los nombres de clave no pueden incluir el carácter de barra diagonal inversa ( ), pero se puede usar cualquier otro \\ carácter imprimible.</span><span class="sxs-lookup"><span data-stu-id="a276c-113">Key names cannot include the backslash character (\\), but any other printable character can be used.</span></span> <span data-ttu-id="a276c-114">Los nombres de valor y los datos pueden incluir el carácter de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a276c-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="a276c-115">El nombre de cada subclave es único con respecto a la clave que está inmediatamente encima de ella en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="a276c-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="a276c-116">Los nombres de clave no se localizan en otros idiomas, aunque los valores pueden ser .</span><span class="sxs-lookup"><span data-stu-id="a276c-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="a276c-117">La siguiente ilustración es una estructura de clave del Registro de ejemplo, tal como se muestra en el Editor del Registro.</span><span class="sxs-lookup"><span data-stu-id="a276c-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![ventana del editor del Registro](images/regtree.png)

<span data-ttu-id="a276c-119">Cada uno de los árboles **bajo Mi PC** es una clave.</span><span class="sxs-lookup"><span data-stu-id="a276c-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="a276c-120">La **clave HKEY \_ LOCAL \_ MACHINE** tiene las siguientes subclaves: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** y **SYSTEM**.</span><span class="sxs-lookup"><span data-stu-id="a276c-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="a276c-121">Cada una de estas claves a su vez tiene subclaves.</span><span class="sxs-lookup"><span data-stu-id="a276c-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="a276c-122">Por ejemplo, la **clave HARDWARE** tiene las subclaves **DESCRIPTION**, **DEVICEMAP** y **RESOURCEMAP**; La **clave DEVICEMAP** tiene varias subclaves, incluido **VIDEO**.</span><span class="sxs-lookup"><span data-stu-id="a276c-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="a276c-123">Cada valor consta de un nombre de valor y sus datos asociados, si los hay.</span><span class="sxs-lookup"><span data-stu-id="a276c-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="a276c-124">**MaxObjectNumber** y **VgaCompatible** son valores que contienen datos bajo la **subclave VIDEO.**</span><span class="sxs-lookup"><span data-stu-id="a276c-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="a276c-125">Un árbol del Registro puede tener 512 niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="a276c-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="a276c-126">Puede crear hasta 32 niveles a la vez a través de una única llamada API del Registro.</span><span class="sxs-lookup"><span data-stu-id="a276c-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a276c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a276c-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a276c-128">[Información general del Registro de Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a276c-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
