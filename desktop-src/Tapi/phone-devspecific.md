---
description: TAPI envía el \_ mensaje Phone DEVSPECIFIC a una aplicación para notificar a la aplicación los eventos específicos del dispositivo que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Mensaje de PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678906"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="d6680-104">Mensaje de teléfono \_ DEVSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="d6680-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="d6680-105">TAPI envía el mensaje **Phone \_ DEVSPECIFIC** a una aplicación para notificar a la aplicación los eventos específicos del dispositivo que se producen en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="d6680-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="d6680-106">El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.</span><span class="sxs-lookup"><span data-stu-id="d6680-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d6680-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6680-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6680-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="d6680-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="d6680-109">Identificador del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="d6680-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d6680-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d6680-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d6680-111">Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="d6680-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d6680-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d6680-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d6680-113">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6680-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="d6680-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d6680-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d6680-115">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6680-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="d6680-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d6680-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d6680-117">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6680-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6680-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6680-118">Return value</span></span>

<span data-ttu-id="d6680-119">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d6680-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6680-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6680-120">Requirements</span></span>



| <span data-ttu-id="d6680-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6680-121">Requirement</span></span> | <span data-ttu-id="d6680-122">Value</span><span class="sxs-lookup"><span data-stu-id="d6680-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d6680-123">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d6680-123">TAPI version</span></span><br/> | <span data-ttu-id="d6680-124">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d6680-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d6680-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6680-125">Header</span></span><br/>       | <dl> <span data-ttu-id="d6680-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6680-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




