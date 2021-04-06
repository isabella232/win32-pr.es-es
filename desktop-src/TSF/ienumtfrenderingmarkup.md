---
title: Interfaz IEnumTfRenderingMarkup
description: La interfaz IEnumTfRenderingMarkup se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante ITfContextRenderingMarkup GetRenderingMarkup y enumera la información de marcado de representación.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup interface Text Services Framework
- IEnumTfRenderingMarkup interface Text Services Framework, descrito
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078163"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="5b42f-106">Interfaz IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5b42f-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="5b42f-107">La interfaz **IEnumTfRenderingMarkup** se implementa mediante el administrador de TSF y la usan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5b42f-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="5b42f-108">Esta interfaz se puede recuperar mediante [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) y enumera la información de marcado de representación.</span><span class="sxs-lookup"><span data-stu-id="5b42f-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="5b42f-109">Métodos IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5b42f-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="5b42f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b42f-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b42f-111">Clonar</span><span class="sxs-lookup"><span data-stu-id="5b42f-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="5b42f-112">El método **IEnumTfRenderingMarkup:: Clone** crea una copia del objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="5b42f-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="5b42f-113">Siguiente</span><span class="sxs-lookup"><span data-stu-id="5b42f-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="5b42f-114">El método **IEnumTfRenderingMarkup:: Next** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="5b42f-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="5b42f-115">Reset</span><span class="sxs-lookup"><span data-stu-id="5b42f-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="5b42f-116">El método **IEnumTfRenderingMarkup:: RESET** restablece el objeto de enumerador moviendo la posición actual al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="5b42f-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="5b42f-117">Skip</span><span class="sxs-lookup"><span data-stu-id="5b42f-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="5b42f-118">El método **IEnumTfRenderingMarkup:: Skip** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="5b42f-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="5b42f-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b42f-119">Members</span></span>

<span data-ttu-id="5b42f-120">La interfaz **IEnumTfRenderingMarkup** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="5b42f-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b42f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b42f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5b42f-122">Esta interfaz no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="5b42f-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="5b42f-123">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="5b42f-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 