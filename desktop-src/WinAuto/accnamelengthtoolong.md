---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704788"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="b71fb-103">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="b71fb-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="b71fb-104">Texto</span><span class="sxs-lookup"><span data-stu-id="b71fb-104">Text</span></span>

<span data-ttu-id="b71fb-105">El nombre del elemento no debe devolver una cadena más larga que el {0} carácter</span><span class="sxs-lookup"><span data-stu-id="b71fb-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="b71fb-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b71fb-106">Type</span></span>

<span data-ttu-id="b71fb-107">Error</span><span class="sxs-lookup"><span data-stu-id="b71fb-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="b71fb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b71fb-108">Description</span></span>

<span data-ttu-id="b71fb-109">El nombre de un elemento contiene demasiados caracteres.</span><span class="sxs-lookup"><span data-stu-id="b71fb-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="b71fb-110">Por ejemplo, el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) que se usa para recuperar el nombre de MSAA de un elemento devuelve una cadena mayor que el límite de 32000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b71fb-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="b71fb-111">Este problema causa problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no descriptivo y no intuitivo.</span><span class="sxs-lookup"><span data-stu-id="b71fb-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="b71fb-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="b71fb-112">Possible causes</span></span>

<span data-ttu-id="b71fb-113">El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="b71fb-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71fb-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b71fb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71fb-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="b71fb-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="b71fb-116">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="b71fb-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




