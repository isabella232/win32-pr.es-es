---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propiedades de SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718711"
---
# <a name="sms-properties"></a><span data-ttu-id="0fc27-103">Propiedades de SMS</span><span class="sxs-lookup"><span data-stu-id="0fc27-103">SMS Properties</span></span>

<span data-ttu-id="0fc27-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de SMS.</span><span class="sxs-lookup"><span data-stu-id="0fc27-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="0fc27-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0fc27-105">Property</span></span>                   | <span data-ttu-id="0fc27-106">VarType</span><span class="sxs-lookup"><span data-stu-id="0fc27-106">VarType</span></span>        | <span data-ttu-id="0fc27-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc27-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc27-108">**\_codificación de SMS de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0fc27-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="0fc27-109">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0fc27-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="0fc27-110">Valor que especifica cómo el controlador codificará el mensaje de texto enviado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="0fc27-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="0fc27-111">Se trata de una propiedad de solo lectura; el cliente no puede especificar el tipo de codificación que usa un dispositivo para enviar mensajes.</span><span class="sxs-lookup"><span data-stu-id="0fc27-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="0fc27-112">Estos valores duplican los valores enumerados de los [**tipos de codificación de SMS de WPD \_ \_ \_**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="0fc27-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="0fc27-113">**\_ \_ carga máxima de SMS de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0fc27-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="0fc27-114">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0fc27-114">**VT\_UI4**</span></span>    | <span data-ttu-id="0fc27-115">Número máximo de bytes que pueden incluirse en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0fc27-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0fc27-116">**\_proveedor de SMS de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0fc27-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="0fc27-117">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0fc27-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="0fc27-118">Nombre del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0fc27-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="0fc27-119">**tiempo de espera de \_ SMS de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0fc27-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="0fc27-120">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0fc27-120">**VT\_UI4**</span></span>    | <span data-ttu-id="0fc27-121">El número de milisegundos hasta que se devuelve un tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="0fc27-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="0fc27-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc27-122">Requirements</span></span>



| <span data-ttu-id="0fc27-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc27-123">Requirement</span></span> | <span data-ttu-id="0fc27-124">Value</span><span class="sxs-lookup"><span data-stu-id="0fc27-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc27-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fc27-125">Header</span></span><br/> | <dl> <span data-ttu-id="0fc27-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fc27-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc27-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fc27-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc27-128">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="0fc27-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




