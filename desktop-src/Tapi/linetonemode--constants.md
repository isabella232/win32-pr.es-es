---
description: Las \_ constantes LINETONEMODE describen diferentes selecciones que se usan al generar tonos de línea.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes de LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690090"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="353d5-103">Constantes de LINETONEMODE \_</span><span class="sxs-lookup"><span data-stu-id="353d5-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="353d5-104">Las **\_ constantes LINETONEMODE** describen diferentes selecciones que se usan al generar tonos de línea.</span><span class="sxs-lookup"><span data-stu-id="353d5-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="353d5-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ beep**</span><span class="sxs-lookup"><span data-stu-id="353d5-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="353d5-106">El tono es un bip, como el que se usa para anunciar el principio de una grabación.</span><span class="sxs-lookup"><span data-stu-id="353d5-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="353d5-107">La definición exacta es el proveedor de servicio definido.</span><span class="sxs-lookup"><span data-stu-id="353d5-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="353d5-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**facturación de LINETONEMODE \_**</span><span class="sxs-lookup"><span data-stu-id="353d5-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="353d5-109">El tono es un tono de información de facturación como un tono de solicitud de tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="353d5-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="353d5-110">La definición exacta es el proveedor de servicio definido.</span><span class="sxs-lookup"><span data-stu-id="353d5-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="353d5-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="353d5-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="353d5-112">El tono es un tono ocupado.</span><span class="sxs-lookup"><span data-stu-id="353d5-112">The tone is a busy tone.</span></span> <span data-ttu-id="353d5-113">La definición exacta es el proveedor de servicio definido.</span><span class="sxs-lookup"><span data-stu-id="353d5-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="353d5-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizado**</span><span class="sxs-lookup"><span data-stu-id="353d5-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="353d5-115">El tono es un tono personalizado definido por sus frecuencias de componentes, de tipo [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span><span class="sxs-lookup"><span data-stu-id="353d5-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="353d5-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**\_timbre LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="353d5-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="353d5-117">El tono es el tono de la timbre.</span><span class="sxs-lookup"><span data-stu-id="353d5-117">The tone is ringback tone.</span></span> <span data-ttu-id="353d5-118">La definición exacta es el proveedor de servicio definido.</span><span class="sxs-lookup"><span data-stu-id="353d5-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="353d5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353d5-119">Remarks</span></span>

<span data-ttu-id="353d5-120">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="353d5-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="353d5-121">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="353d5-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="353d5-122">Estas constantes se utilizan para definir los tonos que se van a generar en banda en una llamada a la parte remota.</span><span class="sxs-lookup"><span data-stu-id="353d5-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="353d5-123">Tenga en cuenta que la detección de tonos de los tonos no personalizados no utiliza estas constantes.</span><span class="sxs-lookup"><span data-stu-id="353d5-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="353d5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="353d5-124">Requirements</span></span>



| <span data-ttu-id="353d5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="353d5-125">Requirement</span></span> | <span data-ttu-id="353d5-126">Value</span><span class="sxs-lookup"><span data-stu-id="353d5-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="353d5-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="353d5-127">TAPI version</span></span><br/> | <span data-ttu-id="353d5-128">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="353d5-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="353d5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="353d5-129">Header</span></span><br/>       | <dl> <span data-ttu-id="353d5-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="353d5-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




