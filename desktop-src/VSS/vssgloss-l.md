---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275424"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="023a7-103">L (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="023a7-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="023a7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="023a7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="023a7-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**Ruta de acceso lógica**</span><span class="sxs-lookup"><span data-stu-id="023a7-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="023a7-106">Mecanismo para describir los componentes de un sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="023a7-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="023a7-107">Se utiliza para expresar las relaciones entre los componentes, en particular su jerarquía.</span><span class="sxs-lookup"><span data-stu-id="023a7-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="023a7-108">Por ejemplo, si un escritor administra varios libros electrónicos, podría asignar rutas de acceso lógicas de " \\ ebook \\ libro1" y " \\ ebook \\ book2" a los componentes del grupo de archivos que contienen cada libro.</span><span class="sxs-lookup"><span data-stu-id="023a7-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="023a7-109">Las rutas de acceso lógicas son necesarias al especificar subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="023a7-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="023a7-110">Por Convención, la barra diagonal inversa " \\ " se usa para separar los elementos de una ruta de acceso lógica.</span><span class="sxs-lookup"><span data-stu-id="023a7-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="023a7-111">Más allá de eso, no hay restricciones en los caracteres que pueden aparecer en una ruta de acceso lógica que no sea **null** .</span><span class="sxs-lookup"><span data-stu-id="023a7-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="023a7-112">Una ruta de acceso lógica puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="023a7-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="023a7-113">Por Convención, se dice que los componentes con rutas de acceso lógicas **nulas** están en el nivel superior de la jerarquía de rutas de acceso lógica de un escritor.</span><span class="sxs-lookup"><span data-stu-id="023a7-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="023a7-114">Vea también [*componente*](vssgloss-c.md), [*subcomponente*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="023a7-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



