---
title: Determinar las clases asociadas a una instancia de objeto
description: Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486627"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="95c62-103">Determinar las clases asociadas a una instancia de objeto</span><span class="sxs-lookup"><span data-stu-id="95c62-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="95c62-104">Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.</span><span class="sxs-lookup"><span data-stu-id="95c62-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95c62-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="95c62-105">Attribute</span></span></th>
<th><span data-ttu-id="95c62-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="95c62-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95c62-107"><strong>structuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="95c62-108">Identifica las clases estructurales y abstractas de las que el objeto es una instancia de.</span><span class="sxs-lookup"><span data-stu-id="95c62-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="95c62-109">Por ejemplo, los valores de un objeto de usuario pueden ser:</span><span class="sxs-lookup"><span data-stu-id="95c62-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="95c62-110"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="95c62-111"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="95c62-112"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="95c62-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c62-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="95c62-115">Identifica las clases incluidas en <strong>structuralObjectClass</strong>, además de las clases auxiliares que se adjuntan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="95c62-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="95c62-116">Por ejemplo, si una &quot; &quot; clase auxiliar de vehículo se adjunta a un objeto de usuario, los valores pueden ser:</span><span class="sxs-lookup"><span data-stu-id="95c62-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="95c62-117"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="95c62-118"><strong>automóvil</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="95c62-119"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="95c62-120"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="95c62-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="95c62-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="95c62-122">Tenga en cuenta que ninguno de estos atributos incluye clases auxiliares que se vinculan estáticamente con las clases de objeto de las que el objeto es una instancia.</span><span class="sxs-lookup"><span data-stu-id="95c62-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="95c62-123">Por ejemplo, la clase auxiliar **securityPrincipal** se vincula estáticamente a la clase **User** porque se incluye en los valores **systemAuxiliaryClass** del objeto **ClassSchema** del usuario; no se incluye en los atributos **objectClass** o **structuralObjectClass** de las instancias de la clase User.</span><span class="sxs-lookup"><span data-stu-id="95c62-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




