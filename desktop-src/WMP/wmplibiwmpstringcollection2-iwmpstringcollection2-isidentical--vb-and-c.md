---
title: IWMPStringCollection2 isIdentical, método
description: El método isIdentical devuelve un valor que indica si el objeto representado por la interfaz proporcionada es igual que el actual.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709113"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="ec00f-106">IWMPStringCollection2:: isIdentical (método)</span><span class="sxs-lookup"><span data-stu-id="ec00f-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="ec00f-107">El método **isIdentical** devuelve un valor que indica si el objeto representado por la interfaz proporcionada es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="ec00f-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec00f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec00f-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="ec00f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec00f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec00f-110">*pIWMPStringCollection2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ec00f-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec00f-111">La interfaz **WMPLib. IWMPStringCollection2** que representa el objeto que se va a comparar con el actual.</span><span class="sxs-lookup"><span data-stu-id="ec00f-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec00f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec00f-112">Return value</span></span>

<span data-ttu-id="ec00f-113">**System. Boolean** que es el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="ec00f-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="ec00f-114">Un valor de **true** indica que los objetos de colección de cadenas son iguales.</span><span class="sxs-lookup"><span data-stu-id="ec00f-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec00f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec00f-115">Remarks</span></span>

<span data-ttu-id="ec00f-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ec00f-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ec00f-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ec00f-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec00f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec00f-118">Requirements</span></span>



| <span data-ttu-id="ec00f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec00f-119">Requirement</span></span> | <span data-ttu-id="ec00f-120">Value</span><span class="sxs-lookup"><span data-stu-id="ec00f-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec00f-121">Versión</span><span class="sxs-lookup"><span data-stu-id="ec00f-121">Version</span></span><br/>   | <span data-ttu-id="ec00f-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ec00f-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ec00f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ec00f-123">Namespace</span></span><br/> | <span data-ttu-id="ec00f-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ec00f-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ec00f-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ec00f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ec00f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ec00f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec00f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec00f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec00f-128">**Interfaz IWMPStringCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ec00f-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





