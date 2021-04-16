---
title: IWMPCdromBurn refreshStatus, método
description: El método refreshStatus actualiza la información de estado de la lista de reproducción actual de la grabación.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- método refreshStatus de Windows Media Player
- método refreshStatus Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718827"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="29bc9-106">IWMPCdromBurn:: refreshStatus (método)</span><span class="sxs-lookup"><span data-stu-id="29bc9-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="29bc9-107">El método **refreshStatus** actualiza la información de estado de la lista de reproducción actual de la grabación.</span><span class="sxs-lookup"><span data-stu-id="29bc9-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bc9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29bc9-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="29bc9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29bc9-109">Parameters</span></span>

<span data-ttu-id="29bc9-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="29bc9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29bc9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29bc9-111">Return value</span></span>

<span data-ttu-id="29bc9-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="29bc9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29bc9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29bc9-113">Remarks</span></span>

<span data-ttu-id="29bc9-114">Debe llamar a este método después de crear o cambiar una lista de reproducción de grabación antes de leer la información de estado o grabar el CD.</span><span class="sxs-lookup"><span data-stu-id="29bc9-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="29bc9-115">Puede comprobar si se requiere una actualización obteniendo el valor de **burnState** y comprobando si hay wmpbsRefreshStatusPending.</span><span class="sxs-lookup"><span data-stu-id="29bc9-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="29bc9-116">La actualización del estado es una operación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="29bc9-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="29bc9-117">Esto significa que puede transcurrir un período largo de tiempo antes de que este método devuelva si la lista de reproducción actual de la grabación es grande y contiene muchos cambios.</span><span class="sxs-lookup"><span data-stu-id="29bc9-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="29bc9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29bc9-118">Requirements</span></span>



| <span data-ttu-id="29bc9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="29bc9-119">Requirement</span></span> | <span data-ttu-id="29bc9-120">Value</span><span class="sxs-lookup"><span data-stu-id="29bc9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29bc9-121">Versión</span><span class="sxs-lookup"><span data-stu-id="29bc9-121">Version</span></span><br/>   | <span data-ttu-id="29bc9-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="29bc9-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="29bc9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29bc9-123">Namespace</span></span><br/> | <span data-ttu-id="29bc9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="29bc9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="29bc9-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="29bc9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="29bc9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="29bc9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29bc9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="29bc9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bc9-128">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="29bc9-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29bc9-129">**IWMPCdromBurn. burnState (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="29bc9-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29bc9-130">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="29bc9-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





