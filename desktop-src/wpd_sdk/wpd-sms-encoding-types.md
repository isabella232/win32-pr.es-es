---
description: El \_ \_ \_ tipo de enumeración de tipos de codificación SMS de WPD describe el tipo de codificación de un mensaje de servicio de mensajes cortos (SMS).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumeración WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650072"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="a9caf-103">\_ \_ Enumeración de tipos de codificación SMS de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a9caf-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="a9caf-104">El tipo de enumeración de **\_ \_ \_ tipos de codificación SMS de WPD** describe el tipo de codificación de un mensaje de servicio de mensajes cortos (SMS).</span><span class="sxs-lookup"><span data-stu-id="a9caf-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9caf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9caf-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="a9caf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a9caf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9caf-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Codificación SMS de \_ 7 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="a9caf-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="a9caf-108">Codificación de siete bits.</span><span class="sxs-lookup"><span data-stu-id="a9caf-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="a9caf-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**CODIFICACIÓN de SMS de \_ \_ 8 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="a9caf-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="a9caf-110">Codificación de ocho bits.</span><span class="sxs-lookup"><span data-stu-id="a9caf-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="a9caf-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Codificación de SMS \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="a9caf-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="a9caf-112">Codificación de dieciséis bits (UTF).</span><span class="sxs-lookup"><span data-stu-id="a9caf-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9caf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9caf-113">Remarks</span></span>

<span data-ttu-id="a9caf-114">Esta enumeración la usa la propiedad de [ \_ \_ codificación de SMS de WPD](sms-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a9caf-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9caf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9caf-115">Requirements</span></span>



| <span data-ttu-id="a9caf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9caf-116">Requirement</span></span> | <span data-ttu-id="a9caf-117">Value</span><span class="sxs-lookup"><span data-stu-id="a9caf-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9caf-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9caf-118">Header</span></span><br/> | <dl> <span data-ttu-id="a9caf-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9caf-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9caf-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9caf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9caf-121">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="a9caf-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




