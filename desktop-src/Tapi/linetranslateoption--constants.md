---
description: La \_ constante de marca de bits LINETRANSLATEOPTION describe una opción usada por la traducción de direcciones.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Constantes de LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690329"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="cee6b-103">Constantes de LINETRANSLATEOPTION \_</span><span class="sxs-lookup"><span data-stu-id="cee6b-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="cee6b-104">La constante de marca de bits **LINETRANSLATEOPTION \_** describe una opción usada por la traducción de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cee6b-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="cee6b-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**</span><span class="sxs-lookup"><span data-stu-id="cee6b-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cee6b-106">Si se define una cadena de espera de llamada de cancelación para la ubicación, si se establece este bit, se insertará esa cadena al principio de la cadena de marcado.</span><span class="sxs-lookup"><span data-stu-id="cee6b-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="cee6b-107">Esto se usa normalmente en las aplicaciones de fax y módem de datos para evitar la interrupción de llamadas por llamadas a los pitidos en espera.</span><span class="sxs-lookup"><span data-stu-id="cee6b-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="cee6b-108">Si no se define ninguna cadena de espera de llamada de cancelación para la ubicación, este bit no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="cee6b-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="cee6b-109">Tenga en cuenta que se recomienda que las aplicaciones que usan este bit también establezcan el \_ bit seguro LINECALLPARAMFLAGS en el miembro **dwCallParamFlags** de la estructura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) que se pasa a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) a través del parámetro *lpCallParams* , de modo que si el dispositivo de línea usa un mecanismo distinto de dígitos que se pueden marcar para suprimir interrupciones de llamadas, se invocará ese mecanismo.</span><span class="sxs-lookup"><span data-stu-id="cee6b-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cee6b-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="cee6b-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cee6b-111">La tarjeta de llamada predeterminada se invalidará con una especificada.</span><span class="sxs-lookup"><span data-stu-id="cee6b-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cee6b-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**</span><span class="sxs-lookup"><span data-stu-id="cee6b-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cee6b-113">Esta opción obliga a que la dirección (número) se traduzca a larga distancia.</span><span class="sxs-lookup"><span data-stu-id="cee6b-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cee6b-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**</span><span class="sxs-lookup"><span data-stu-id="cee6b-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cee6b-115">Esta opción obliga a que el número (dirección) se traduzca como local.</span><span class="sxs-lookup"><span data-stu-id="cee6b-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cee6b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cee6b-116">Remarks</span></span>

<span data-ttu-id="cee6b-117">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="cee6b-117">No extensibility.</span></span> <span data-ttu-id="cee6b-118">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="cee6b-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee6b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cee6b-119">Requirements</span></span>



| <span data-ttu-id="cee6b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee6b-120">Requirement</span></span> | <span data-ttu-id="cee6b-121">Value</span><span class="sxs-lookup"><span data-stu-id="cee6b-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cee6b-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cee6b-122">TAPI version</span></span><br/> | <span data-ttu-id="cee6b-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cee6b-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cee6b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cee6b-124">Header</span></span><br/>       | <dl> <span data-ttu-id="cee6b-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cee6b-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee6b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cee6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee6b-127">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="cee6b-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="cee6b-128">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="cee6b-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="cee6b-129">**LINETRANSLATEOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="cee6b-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




