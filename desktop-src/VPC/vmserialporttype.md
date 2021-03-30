---
title: Enumeración VMSerialPortType (VPCCOMInterfaces. h)
description: Especifica el tipo de puerto serie.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- Enumeración de VMSerialPortType Virtual PC
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534756"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="e485d-104">Enumeración VMSerialPortType</span><span class="sxs-lookup"><span data-stu-id="e485d-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="e485d-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e485d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e485d-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e485d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e485d-107">Especifica el tipo de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="e485d-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e485d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e485d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="e485d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="e485d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e485d-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort \_ denominaba hostport**</span><span class="sxs-lookup"><span data-stu-id="e485d-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="e485d-111">Un puerto serie del host.</span><span class="sxs-lookup"><span data-stu-id="e485d-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e485d-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort \_ TextFile**</span><span class="sxs-lookup"><span data-stu-id="e485d-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="e485d-113">Un archivo de texto de host.</span><span class="sxs-lookup"><span data-stu-id="e485d-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="e485d-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="e485d-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="e485d-115">Una canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="e485d-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="e485d-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort \_ null**</span><span class="sxs-lookup"><span data-stu-id="e485d-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="e485d-117">Un puerto serie **nulo** (descarta todos los bits enviados a él).</span><span class="sxs-lookup"><span data-stu-id="e485d-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e485d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e485d-118">Requirements</span></span>



| <span data-ttu-id="e485d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e485d-119">Requirement</span></span> | <span data-ttu-id="e485d-120">Value</span><span class="sxs-lookup"><span data-stu-id="e485d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e485d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e485d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e485d-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e485d-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e485d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e485d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e485d-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e485d-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e485d-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e485d-125">End of client support</span></span><br/>    | <span data-ttu-id="e485d-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e485d-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e485d-127">Producto</span><span class="sxs-lookup"><span data-stu-id="e485d-127">Product</span></span><br/>                  | <span data-ttu-id="e485d-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e485d-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e485d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e485d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e485d-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e485d-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e485d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e485d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e485d-132">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="e485d-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

