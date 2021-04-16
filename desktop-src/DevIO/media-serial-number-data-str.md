---
description: Contiene el número de serie de un dispositivo USB. Lo utiliza el código de control de número de serie del medio de almacenamiento de IOCTL \_ \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Estructura de MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649321"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="37f62-104">\_Estructura de \_ datos de número de serie de medios \_</span><span class="sxs-lookup"><span data-stu-id="37f62-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="37f62-105">Contiene el número de serie de un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="37f62-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="37f62-106">Lo utiliza el código de control de [**\_ número de \_ \_ \_ serie \_ del medio de almacenamiento de ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .</span><span class="sxs-lookup"><span data-stu-id="37f62-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f62-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37f62-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="37f62-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="37f62-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37f62-109">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="37f62-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="37f62-110">Tamaño de la cadena de **SerialNumberData** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="37f62-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37f62-111">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="37f62-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="37f62-112">Estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37f62-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="37f62-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="37f62-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="37f62-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="37f62-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="37f62-115">**SerialNumberData**</span><span class="sxs-lookup"><span data-stu-id="37f62-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="37f62-116">El número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37f62-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37f62-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37f62-117">Remarks</span></span>

<span data-ttu-id="37f62-118">No hay ningún archivo de encabezado disponible para la estructura de **datos del número de serie del medio \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="37f62-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="37f62-119">Incluya la definición de la estructura en la parte superior de esta página en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="37f62-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f62-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f62-120">Requirements</span></span>



| <span data-ttu-id="37f62-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f62-121">Requirement</span></span> | <span data-ttu-id="37f62-122">Value</span><span class="sxs-lookup"><span data-stu-id="37f62-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="37f62-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37f62-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37f62-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37f62-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="37f62-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37f62-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37f62-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37f62-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37f62-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="37f62-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f62-128">**el \_ almacenamiento ioctl \_ obtiene el número de \_ serie del medio \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37f62-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




