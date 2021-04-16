---
title: IWMPCdromBurn startBurn, método
description: El método startBurn graba el CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- método startBurn de Windows Media Player
- método startBurn Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718826"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="ec610-106">IWMPCdromBurn:: startBurn (método)</span><span class="sxs-lookup"><span data-stu-id="ec610-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="ec610-107">El método **startBurn** graba el CD.</span><span class="sxs-lookup"><span data-stu-id="ec610-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec610-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec610-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="ec610-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec610-109">Parameters</span></span>

<span data-ttu-id="ec610-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec610-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec610-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec610-111">Return value</span></span>

<span data-ttu-id="ec610-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec610-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec610-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec610-113">Remarks</span></span>

<span data-ttu-id="ec610-114">El valor de **burnstate** debe ser WmpbsReady o wmpbsStopped antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="ec610-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="ec610-115">Este método no funcionará si la unidad de CD no es una grabadora o si no se puede escribir en el disco de la unidad.</span><span class="sxs-lookup"><span data-stu-id="ec610-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="ec610-116">Use **isavailable** para determinar si se puede grabar un CD.</span><span class="sxs-lookup"><span data-stu-id="ec610-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec610-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec610-117">Requirements</span></span>



| <span data-ttu-id="ec610-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec610-118">Requirement</span></span> | <span data-ttu-id="ec610-119">Value</span><span class="sxs-lookup"><span data-stu-id="ec610-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec610-120">Versión</span><span class="sxs-lookup"><span data-stu-id="ec610-120">Version</span></span><br/>   | <span data-ttu-id="ec610-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ec610-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ec610-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ec610-122">Namespace</span></span><br/> | <span data-ttu-id="ec610-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ec610-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ec610-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ec610-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ec610-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ec610-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec610-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec610-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec610-127">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ec610-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec610-128">**IWMPCdromBurn. burnState (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ec610-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec610-129">**IWMPCdromBurn. isAvailable (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ec610-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec610-130">**IWMPCdromBurn. stopBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ec610-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





