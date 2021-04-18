---
description: El \_ \_ tipo de enumeración SMS Message Types describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Enumeración SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718712"
---
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="73f52-103">\_Enumeración de tipos de mensajes SMS \_</span><span class="sxs-lookup"><span data-stu-id="73f52-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="73f52-104">El tipo de enumeración **SMS \_ Message \_** Types describe el tipo de contenido de un mensaje de servicio de mensajes cortos (SMS).</span><span class="sxs-lookup"><span data-stu-id="73f52-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73f52-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="73f52-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="73f52-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73f52-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**\_mensaje de texto SMS \_**</span><span class="sxs-lookup"><span data-stu-id="73f52-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="73f52-108">Un mensaje de texto.</span><span class="sxs-lookup"><span data-stu-id="73f52-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="73f52-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_mensaje binario de SMS \_**</span><span class="sxs-lookup"><span data-stu-id="73f52-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="73f52-110">Un mensaje binario.</span><span class="sxs-lookup"><span data-stu-id="73f52-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73f52-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73f52-111">Remarks</span></span>

<span data-ttu-id="73f52-112">Esta enumeración la usa el comando de [**envío de SMS de comandos de WPD \_ \_ \_**](wpd-command-sms-send-command.md).</span><span class="sxs-lookup"><span data-stu-id="73f52-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73f52-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73f52-113">Requirements</span></span>



| <span data-ttu-id="73f52-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f52-114">Requirement</span></span> | <span data-ttu-id="73f52-115">Value</span><span class="sxs-lookup"><span data-stu-id="73f52-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f52-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73f52-116">Header</span></span><br/> | <dl> <span data-ttu-id="73f52-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f52-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73f52-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="73f52-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f52-119">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="73f52-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




