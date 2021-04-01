---
title: Enumeración RAS_PARAMS_FORMAT (rassapi. h)
description: El \_ \_ tipo de enumeración de formato de los parámetros de Ras se usa en la estructura de parámetros de Ras \_ para indicar el tipo de datos asociado a una clave específica del medio.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT enumeración de RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150523"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="09e21-104">\_Enumeración de formato de parámetros ras \_</span><span class="sxs-lookup"><span data-stu-id="09e21-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="09e21-105">\[La enumeración de **\_ \_ formato** de los parámetros de Ras no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="09e21-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="09e21-106">El tipo de enumeración de **\_ \_ formato** de los parámetros de Ras se usa en la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) para indicar el tipo de datos asociado a una clave específica del medio.</span><span class="sxs-lookup"><span data-stu-id="09e21-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e21-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09e21-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="09e21-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="09e21-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09e21-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span><span class="sxs-lookup"><span data-stu-id="09e21-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="09e21-110">Indica que los datos asociados a la clave son un número.</span><span class="sxs-lookup"><span data-stu-id="09e21-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="09e21-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span><span class="sxs-lookup"><span data-stu-id="09e21-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="09e21-112">Indica que los datos asociados a la clave son una cadena.</span><span class="sxs-lookup"><span data-stu-id="09e21-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09e21-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e21-113">Requirements</span></span>



| <span data-ttu-id="09e21-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e21-114">Requirement</span></span> | <span data-ttu-id="09e21-115">Value</span><span class="sxs-lookup"><span data-stu-id="09e21-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09e21-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09e21-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09e21-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="09e21-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09e21-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09e21-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="09e21-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="09e21-120">End of client support</span></span><br/>    | <span data-ttu-id="09e21-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="09e21-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="09e21-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="09e21-122">End of server support</span></span><br/>    | <span data-ttu-id="09e21-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09e21-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="09e21-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09e21-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e21-125"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e21-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e21-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="09e21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e21-127">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="09e21-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="09e21-128">Enumeraciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="09e21-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="09e21-129">**parámetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="09e21-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





