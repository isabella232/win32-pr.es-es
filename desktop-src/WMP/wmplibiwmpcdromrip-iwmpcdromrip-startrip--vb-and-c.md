---
title: IWMPCdromRip startRip, método
description: El método startRip RIP el CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- método startRip de Windows Media Player
- método startRip Windows Media Player, interfaz IWMPCdromRip
- Interfaz IWMPCdromRip Windows Media Player, método startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649912"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="cdd09-106">IWMPCdromRip:: startRip (método)</span><span class="sxs-lookup"><span data-stu-id="cdd09-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="cdd09-107">El método **startRip** RIP el CD.</span><span class="sxs-lookup"><span data-stu-id="cdd09-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdd09-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="cdd09-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdd09-109">Parameters</span></span>

<span data-ttu-id="cdd09-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cdd09-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdd09-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdd09-111">Return value</span></span>

<span data-ttu-id="cdd09-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cdd09-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd09-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdd09-113">Remarks</span></span>

<span data-ttu-id="cdd09-114">La copia desde CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cdd09-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="cdd09-115">El contenido copiado se agrega automáticamente a la biblioteca según las preferencias del usuario.</span><span class="sxs-lookup"><span data-stu-id="cdd09-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="cdd09-116">Para obtener más información acerca de las preferencias de usuario para la copia desde CD, consulte "copiar música desde CDs" en la ayuda de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cdd09-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd09-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdd09-117">Requirements</span></span>



| <span data-ttu-id="cdd09-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd09-118">Requirement</span></span> | <span data-ttu-id="cdd09-119">Value</span><span class="sxs-lookup"><span data-stu-id="cdd09-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd09-120">Versión</span><span class="sxs-lookup"><span data-stu-id="cdd09-120">Version</span></span><br/>   | <span data-ttu-id="cdd09-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="cdd09-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="cdd09-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cdd09-122">Namespace</span></span><br/> | <span data-ttu-id="cdd09-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cdd09-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cdd09-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="cdd09-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cdd09-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd09-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd09-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdd09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd09-127">**Interfaz IWMPCdromRip (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cdd09-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cdd09-128">**IWMPCdromRip.stopRip**</span><span class="sxs-lookup"><span data-stu-id="cdd09-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cdd09-129">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="cdd09-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





