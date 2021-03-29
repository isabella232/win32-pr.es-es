---
description: Se envía el mensaje APPNEWCALLHUB de línea de TAPI \_ para informar a una aplicación cuando se ha creado un nuevo centro de llamadas.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Mensaje de LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680773"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="17e30-103">Mensaje de línea \_ APPNEWCALLHUB</span><span class="sxs-lookup"><span data-stu-id="17e30-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="17e30-104">Se envía el mensaje **\_ APPNEWCALLHUB de línea** de TAPI para informar a una aplicación cuando se ha creado un nuevo centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="17e30-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="17e30-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17e30-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e30-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="17e30-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="17e30-107">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="17e30-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="17e30-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="17e30-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="17e30-109">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="17e30-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="17e30-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="17e30-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="17e30-111">Nivel de seguimiento en el nuevo concentrador, tal y como se define en una de las [**\_ constantes de LINECALLHUBTRACKING**](linecallhubtracking--constants.md).</span><span class="sxs-lookup"><span data-stu-id="17e30-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e30-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17e30-112">Return value</span></span>

<span data-ttu-id="17e30-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="17e30-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e30-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17e30-114">Remarks</span></span>

<span data-ttu-id="17e30-115">Este mensaje se origina con TAPI en lugar de con un proveedor de servicios, por lo que no hay ningún mensaje TSPI correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17e30-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e30-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e30-116">Requirements</span></span>



| <span data-ttu-id="17e30-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e30-117">Requirement</span></span> | <span data-ttu-id="17e30-118">Value</span><span class="sxs-lookup"><span data-stu-id="17e30-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="17e30-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="17e30-119">TAPI version</span></span><br/> | <span data-ttu-id="17e30-120">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="17e30-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="17e30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17e30-121">Header</span></span><br/>       | <dl> <span data-ttu-id="17e30-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e30-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




