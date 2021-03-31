---
title: Árboles de dominio
description: Un árbol de dominios se compone de varios dominios que comparten un esquema y una configuración comunes, formando un espacio de nombres contiguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- árbol de dominios Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268294"
---
# <a name="domain-trees"></a><span data-ttu-id="8e01b-104">Árboles de dominio</span><span class="sxs-lookup"><span data-stu-id="8e01b-104">Domain Trees</span></span>

<span data-ttu-id="8e01b-105">Un *árbol de dominios* se compone de varios dominios que comparten un esquema y una configuración comunes, formando un espacio de nombres contiguo.</span><span class="sxs-lookup"><span data-stu-id="8e01b-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="8e01b-106">Los dominios de un árbol también se vinculan entre sí mediante relaciones de confianza.</span><span class="sxs-lookup"><span data-stu-id="8e01b-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="8e01b-107">Active Directory es un conjunto de uno o más árboles.</span><span class="sxs-lookup"><span data-stu-id="8e01b-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="8e01b-108">Los árboles se pueden ver de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="8e01b-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="8e01b-109">Una vista son las relaciones de confianza entre los dominios.</span><span class="sxs-lookup"><span data-stu-id="8e01b-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="8e01b-110">La otra vista es el espacio de nombres del árbol de dominios.</span><span class="sxs-lookup"><span data-stu-id="8e01b-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="8e01b-111">Ver relaciones de confianza</span><span class="sxs-lookup"><span data-stu-id="8e01b-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="8e01b-112">Puede dibujar un diagrama de un árbol de dominios en función de los dominios individuales y la relación de confianza existente.</span><span class="sxs-lookup"><span data-stu-id="8e01b-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="8e01b-113">Windows 2000 establece relaciones de confianza entre dominios basados en el protocolo de seguridad Kerberos.</span><span class="sxs-lookup"><span data-stu-id="8e01b-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="8e01b-114">La confianza Kerberos es transitiva y jerárquica: Si el dominio A confía en el dominio B y el dominio B confía en el dominio C, el dominio A confía en el dominio C.</span><span class="sxs-lookup"><span data-stu-id="8e01b-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![relación de confianza del árbol de dominios](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="8e01b-116">Ver el espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e01b-116">Viewing the Namespace</span></span>

<span data-ttu-id="8e01b-117">También puede dibujar un diagrama de un árbol de dominios basado en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8e01b-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="8e01b-118">Puede determinar el nombre distintivo de un objeto siguiendo la ruta de acceso hacia arriba en la jerarquía del espacio de nombres del árbol de dominios.</span><span class="sxs-lookup"><span data-stu-id="8e01b-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="8e01b-119">Esta vista es útil para agrupar objetos en una jerarquía lógica.</span><span class="sxs-lookup"><span data-stu-id="8e01b-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="8e01b-120">La principal ventaja de un espacio de nombres contiguo es que una búsqueda profunda desde la raíz del espacio de nombres busca en toda la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="8e01b-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![árbol de dominio de espacio de nombres](images/namespace.png)

 

 




