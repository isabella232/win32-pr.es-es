---
description: Contiene datos que describen un experto cuando se inicia.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Estructura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000941"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="0edf4-103">Estructura EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="0edf4-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="0edf4-104">La estructura **EXPERTSTARTUPINFO** contiene datos que describen un experto cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="0edf4-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edf4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0edf4-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="0edf4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0edf4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0edf4-107">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="0edf4-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-108">Marcas que describen el experto.</span><span class="sxs-lookup"><span data-stu-id="0edf4-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-109">**hCapture**</span><span class="sxs-lookup"><span data-stu-id="0edf4-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-110">Identificador de una captura.</span><span class="sxs-lookup"><span data-stu-id="0edf4-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-111">**szCaptureFile**</span><span class="sxs-lookup"><span data-stu-id="0edf4-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-112">Nombre del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="0edf4-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-113">**dwFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="0edf4-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-114">Número de marco.</span><span class="sxs-lookup"><span data-stu-id="0edf4-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-115">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="0edf4-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-116">Identificador del protocolo.</span><span class="sxs-lookup"><span data-stu-id="0edf4-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-117">**lpPropertyInst**</span><span class="sxs-lookup"><span data-stu-id="0edf4-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-118">Puntero a una estructura [**PROPERTYINST**](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="0edf4-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-119">**sBitfield**</span><span class="sxs-lookup"><span data-stu-id="0edf4-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edf4-120">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="0edf4-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-121">Solo se usa si el miembro de **calificador** de la estructura [**PROPERTYINST**](propertyinst.md) está establecido en las marcas propia \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0edf4-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="0edf4-122">**Despedida**</span><span class="sxs-lookup"><span data-stu-id="0edf4-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="0edf4-123">Solo se usa si el miembro de **calificador** de la estructura [**PROPERTYINST**](propertyinst.md) está establecido en las marcas propia \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0edf4-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0edf4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edf4-124">Requirements</span></span>



| <span data-ttu-id="0edf4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edf4-125">Requirement</span></span> | <span data-ttu-id="0edf4-126">Value</span><span class="sxs-lookup"><span data-stu-id="0edf4-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0edf4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0edf4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0edf4-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0edf4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0edf4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0edf4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0edf4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0edf4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0edf4-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0edf4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0edf4-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0edf4-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




