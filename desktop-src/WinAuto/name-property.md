---
title: Propiedad Name
description: La propiedad Name es una cadena utilizada por los clientes para identificar, buscar o anunciar un objeto para el usuario. Todos los objetos admiten la propiedad Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704664"
---
# <a name="name-property"></a><span data-ttu-id="bc030-104">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="bc030-104">Name Property</span></span>

<span data-ttu-id="bc030-105">La propiedad **Name** es una cadena utilizada por los clientes para identificar, buscar o anunciar un objeto para el usuario.</span><span class="sxs-lookup"><span data-stu-id="bc030-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="bc030-106">Todos los objetos admiten la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="bc030-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="bc030-107">Por ejemplo, el texto de un control de botón es su nombre, mientras que el nombre de un cuadro de lista o un control de edición es el texto estático que precede inmediatamente al control en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="bc030-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="bc030-108">Incluso los objetos gráficos que no muestran un nombre proporcionan texto cuando se consulta la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="bc030-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="bc030-109">La propiedad **Name** se recupera llamando a [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span><span class="sxs-lookup"><span data-stu-id="bc030-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="bc030-110">Seleccionar nombres</span><span class="sxs-lookup"><span data-stu-id="bc030-110">Selecting Names</span></span>

<span data-ttu-id="bc030-111">El nombre de un objeto debe ser intuitivo para que los usuarios sepan el significado o el propósito del objeto.</span><span class="sxs-lookup"><span data-stu-id="bc030-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="bc030-112">Además, la propiedad **Name** debe ser única relativa a cualquier objeto relacionado en el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="bc030-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="bc030-113">La navegación dentro de las tablas presenta problemas especialmente difíciles para algunos usuarios.</span><span class="sxs-lookup"><span data-stu-id="bc030-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="bc030-114">Por lo tanto, los desarrolladores de servidor deben hacer que los nombres de celda de tabla sean lo más descriptivos posible.</span><span class="sxs-lookup"><span data-stu-id="bc030-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="bc030-115">Por ejemplo, puede crear un nombre de celda combinando los nombres de la fila y la columna que ocupa, como "a1".</span><span class="sxs-lookup"><span data-stu-id="bc030-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="bc030-116">Sin embargo, suele ser mejor usar nombres más descriptivos, como "Nancy, febrero", donde "Nancy" es la fila actual y "febrero" es la columna actual.</span><span class="sxs-lookup"><span data-stu-id="bc030-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="bc030-117">Delegación de solicitudes</span><span class="sxs-lookup"><span data-stu-id="bc030-117">Delegating Requests</span></span>

<span data-ttu-id="bc030-118">Si un objeto no tiene acceso a su propiedad **Name** , delega las solicitudes a su elemento primario, identificando por su identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="bc030-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="bc030-119">Por ejemplo, si un cliente llama a la propiedad de **nombre** de un control de edición, el control de edición delega la consulta a su elemento primario, que devuelve el valor del control de texto estático que etiqueta el control de edición.</span><span class="sxs-lookup"><span data-stu-id="bc030-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




