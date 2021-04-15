---
description: Define los patrones de bits que habilitan los planos de recorte definidos por el usuario. Estas macros se definen como una comodidad cuando se establecen valores para el \_ Estado de representación de D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424355"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="c394f-104">D3DCLIPPLANEn (macro)</span><span class="sxs-lookup"><span data-stu-id="c394f-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="c394f-105">Define los patrones de bits que habilitan los planos de recorte definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c394f-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="c394f-106">Estas macros se definen como una comodidad cuando se establecen valores para el \_ Estado de representación de D3DRS CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="c394f-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c394f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c394f-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="c394f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c394f-108">Parameters</span></span>

<span data-ttu-id="c394f-109">Esta macro no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c394f-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c394f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c394f-110">Return value</span></span>

<span data-ttu-id="c394f-111">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c394f-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c394f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c394f-112">Remarks</span></span>

<span data-ttu-id="c394f-113">Los planos de recorte definidos por el usuario se habilitan cuando el valor establecido en el estado de representación de D3DRS \_ CLIPPLANEENABLE contiene uno o varios bits de conjunto (es decir, no es 0).</span><span class="sxs-lookup"><span data-stu-id="c394f-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="c394f-114">El valor del estado de representación no es importante; el sistema no interpreta el valor como un número.</span><span class="sxs-lookup"><span data-stu-id="c394f-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="c394f-115">En su lugar, el valor habilita el plano de recorte cuyo bit correspondiente está establecido.</span><span class="sxs-lookup"><span data-stu-id="c394f-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="c394f-116">Bit 0 controla el estado del primer plano de recorte (en el índice 0), el bit 1 el segundo plano, etc.</span><span class="sxs-lookup"><span data-stu-id="c394f-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="c394f-117">Los patrones de bits creados por estas macros se pueden combinar mediante una operación OR lógica para habilitar simultáneamente varios planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="c394f-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="c394f-118">Si se omite una de estas macros de la combinación, se deshabilita de manera eficaz el plano de recorte en dicho índice.</span><span class="sxs-lookup"><span data-stu-id="c394f-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c394f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c394f-119">Requirements</span></span>



| <span data-ttu-id="c394f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c394f-120">Requirement</span></span> | <span data-ttu-id="c394f-121">Value</span><span class="sxs-lookup"><span data-stu-id="c394f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c394f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c394f-122">Header</span></span><br/> | <dl> <span data-ttu-id="c394f-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c394f-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c394f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c394f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c394f-125">Macros</span><span class="sxs-lookup"><span data-stu-id="c394f-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




