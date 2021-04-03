---
title: Interfaz ITfContextRenderingMarkup
description: La interfaz ITfContextRenderingMarkup se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante IQueryInterface del objeto ITfContext. Esta interfaz ayuda a la aplicación a enumerar la información de representación.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfContextRenderingMarkup interface Text Services Framework
- ITfContextRenderingMarkup interface Text Services Framework, descrito
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904691"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="5e75e-107">Interfaz ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5e75e-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="5e75e-108">La interfaz **ITfContextRenderingMarkup** se implementa mediante el administrador de TSF y la usan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5e75e-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="5e75e-109">Esta interfaz se puede recuperar mediante IQueryInterface del objeto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) .</span><span class="sxs-lookup"><span data-stu-id="5e75e-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="5e75e-110">Esta interfaz ayuda a la aplicación a enumerar la información de representación.</span><span class="sxs-lookup"><span data-stu-id="5e75e-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="5e75e-111">Métodos ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5e75e-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="5e75e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e75e-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="5e75e-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5e75e-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="5e75e-114">Recupera un enumerador de los marcas de representación para el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="5e75e-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="5e75e-115">FindNextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5e75e-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="5e75e-116">Esta función no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5e75e-116">This function is not implemented.</span></span> <span data-ttu-id="5e75e-117">Siempre devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5e75e-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="5e75e-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e75e-118">Members</span></span>

<span data-ttu-id="5e75e-119">La interfaz **ITfContextRenderingMarkup** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="5e75e-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e75e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e75e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e75e-121">Esta interfaz no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="5e75e-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="5e75e-122">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="5e75e-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 