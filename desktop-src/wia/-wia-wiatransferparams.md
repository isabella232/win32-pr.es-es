---
description: 'El WiaTransferParams se transmite a una aplicación durante una transferencia de datos mediante el sistema de tiempo de ejecución de adquisición de imágenes de Windows (WIA) al método IWiaTransferCallback:: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estructura WiaTransferParams (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696494"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="45f92-103">Estructura WiaTransferParams</span><span class="sxs-lookup"><span data-stu-id="45f92-103">WiaTransferParams structure</span></span>

<span data-ttu-id="45f92-104">El **WiaTransferParams** se transmite a una aplicación durante una transferencia de datos mediante el sistema de tiempo de ejecución de adquisición de imágenes de Windows (WIA) al método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .</span><span class="sxs-lookup"><span data-stu-id="45f92-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45f92-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="45f92-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="45f92-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="45f92-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="45f92-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="45f92-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="45f92-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="45f92-109">Indica el estado de la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="45f92-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="45f92-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_Estado de \_ mensaje de transferencia de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="45f92-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="45f92-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ final \_ de la secuencia del mensaje de transferencia de \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="45f92-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="45f92-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fin \_ de la transferencia del mensaje de transferencia de \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="45f92-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="45f92-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_Estado del \_ dispositivo de mensajes de transferencia WIA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45f92-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="45f92-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ Página nuevo mensaje de transferencia de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="45f92-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="45f92-115">**lPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="45f92-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="45f92-116">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="45f92-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="45f92-117">Indica el progreso de la transferencia de datos como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="45f92-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="45f92-118">**ulTransferredBytes**</span><span class="sxs-lookup"><span data-stu-id="45f92-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="45f92-119">Tipo: **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="45f92-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="45f92-120">Indica la cantidad de datos transferidos.</span><span class="sxs-lookup"><span data-stu-id="45f92-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="45f92-121">**hrErrorStatus**</span><span class="sxs-lookup"><span data-stu-id="45f92-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="45f92-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45f92-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="45f92-123">El estado, o estado de error, del dispositivo establecido por el controlador; por ejemplo, "preparando".</span><span class="sxs-lookup"><span data-stu-id="45f92-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45f92-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f92-124">Requirements</span></span>



| <span data-ttu-id="45f92-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f92-125">Requirement</span></span> | <span data-ttu-id="45f92-126">Value</span><span class="sxs-lookup"><span data-stu-id="45f92-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="45f92-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45f92-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45f92-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45f92-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="45f92-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45f92-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45f92-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45f92-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="45f92-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45f92-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f92-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f92-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




