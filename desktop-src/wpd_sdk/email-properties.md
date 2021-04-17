---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de correo electrónico.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propiedades de correo electrónico (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680387"
---
# <a name="email-properties"></a><span data-ttu-id="1a521-103">Propiedades de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a521-103">Email Properties</span></span>

<span data-ttu-id="1a521-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="1a521-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a521-105">Property</span></span>                         | <span data-ttu-id="1a521-106">VarType</span><span class="sxs-lookup"><span data-stu-id="1a521-106">VarType</span></span>        | <span data-ttu-id="1a521-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a521-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a521-108">**\_línea CCO de correo electrónico de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="1a521-109">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1a521-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1a521-110">Destinatarios de CCO del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="1a521-111">Los destinatarios CCO reciben una copia del mensaje de correo electrónico, pero sus nombres no se muestran como destinatarios.</span><span class="sxs-lookup"><span data-stu-id="1a521-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="1a521-112">**\_línea CC de correo electrónico de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="1a521-113">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1a521-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1a521-114">Destinatarios de CC del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="1a521-115">Los destinatarios de CC reciben una copia del mensaje de correo electrónico y sus nombres se muestran como destinatarios.</span><span class="sxs-lookup"><span data-stu-id="1a521-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="1a521-116">**el \_ correo electrónico de WPD \_ tiene \_ datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="1a521-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="1a521-117">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1a521-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="1a521-118">Valor booleano que especifica si este mensaje de correo electrónico tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1a521-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="1a521-119">**se \_ ha \_ \_ leído el correo electrónico de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="1a521-120">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1a521-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="1a521-121">Valor booleano que especifica si se ha leído este mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="1a521-122">**\_hora de recepción de correo electrónico de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="1a521-123">**fecha de VT \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-123">**VT\_DATE**</span></span>   | <span data-ttu-id="1a521-124">Valor que especifica cuándo se recibió el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="1a521-125">**\_dirección del remitente de correo electrónico de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a521-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="1a521-126">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1a521-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1a521-127">La dirección de correo electrónico del remitente.</span><span class="sxs-lookup"><span data-stu-id="1a521-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="1a521-128">**\_correo electrónico \_ de WPD en \_ línea**</span><span class="sxs-lookup"><span data-stu-id="1a521-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="1a521-129">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1a521-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1a521-130">Los destinatarios principales del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a521-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="1a521-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a521-131">Requirements</span></span>



| <span data-ttu-id="1a521-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a521-132">Requirement</span></span> | <span data-ttu-id="1a521-133">Value</span><span class="sxs-lookup"><span data-stu-id="1a521-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a521-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a521-134">Header</span></span><br/> | <dl> <span data-ttu-id="1a521-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a521-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a521-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a521-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a521-137">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="1a521-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




