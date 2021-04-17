---
description: El \_ mensaje de creación del teléfono TAPI se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Mensaje de PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679060"
---
# <a name="phone_create-message"></a><span data-ttu-id="4da49-103">Mensaje de creación de teléfono \_</span><span class="sxs-lookup"><span data-stu-id="4da49-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="4da49-104">El mensaje **de \_ creación del teléfono** TAPI se envía para informar a las aplicaciones de la creación de un nuevo dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="4da49-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4da49-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4da49-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da49-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="4da49-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="4da49-107">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="4da49-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4da49-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4da49-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4da49-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="4da49-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4da49-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4da49-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4da49-111">*HDeviceID* del dispositivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="4da49-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="4da49-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4da49-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4da49-113">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="4da49-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4da49-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4da49-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4da49-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="4da49-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da49-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4da49-116">Return value</span></span>

<span data-ttu-id="4da49-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4da49-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da49-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4da49-118">Remarks</span></span>

<span data-ttu-id="4da49-119">A las aplicaciones que negociaron la versión de API 1,3 se les envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que especifica PHONESTATE \_ reinit, que les obliga a apagar su uso de la API y llama a [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) de nuevo para obtener el nuevo número de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4da49-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="4da49-120">Sin embargo, la versión 1,4 y posteriores de TAPI no requieren que se cierren todas las aplicaciones antes de permitir que las aplicaciones se reinicialicen. la reinicialización puede realizarse inmediatamente cuando se crea un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4da49-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="4da49-121">Las aplicaciones que admiten la versión 1,4 o posterior de TAPI recibirán un mensaje de **\_ creación de teléfono** .</span><span class="sxs-lookup"><span data-stu-id="4da49-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="4da49-122">Esto informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4da49-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="4da49-123">A continuación, la aplicación puede elegir si desea o no intentar trabajar con el nuevo dispositivo en su momento.</span><span class="sxs-lookup"><span data-stu-id="4da49-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da49-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da49-124">Requirements</span></span>



| <span data-ttu-id="4da49-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da49-125">Requirement</span></span> | <span data-ttu-id="4da49-126">Value</span><span class="sxs-lookup"><span data-stu-id="4da49-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4da49-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4da49-127">TAPI version</span></span><br/> | <span data-ttu-id="4da49-128">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4da49-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4da49-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4da49-129">Header</span></span><br/>       | <dl> <span data-ttu-id="4da49-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da49-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da49-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4da49-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da49-132">**Estado del teléfono \_**</span><span class="sxs-lookup"><span data-stu-id="4da49-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="4da49-133">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="4da49-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="4da49-134">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="4da49-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




