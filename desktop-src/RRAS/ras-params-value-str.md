---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: La \_ \_ Unión de valores de parámetros de Ras se usa en la estructura de parámetros de Ras \_ para almacenar los datos asociados a un parámetro específico del medio.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS de RAS_PARAMS_VALUE Union
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149869"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="2ff41-104">Valores de parámetros de RAS \_ \_ Union</span><span class="sxs-lookup"><span data-stu-id="2ff41-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="2ff41-105">\[La Unión de **\_ \_ valores de parámetros de Ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="2ff41-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="2ff41-106">La Unión de **\_ \_ valores** de parámetros de Ras se usa en la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) para almacenar los datos asociados a un parámetro específico del medio.</span><span class="sxs-lookup"><span data-stu-id="2ff41-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="2ff41-107">El miembro de **\_ tipo P** de la estructura de parámetros de Ras usa un valor de la enumeración de [**\_ \_ formato**](ras-params-format-str.md) de **\_ parámetros** de ras para indicar el tipo de valor almacenado actualmente en el valor de los **\_ parámetros \_ de Ras**.</span><span class="sxs-lookup"><span data-stu-id="2ff41-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ff41-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="2ff41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ff41-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ff41-110">**Number**</span><span class="sxs-lookup"><span data-stu-id="2ff41-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="2ff41-111">Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamNumber, el miembro **Number** contiene el valor del parámetro específico del medio.</span><span class="sxs-lookup"><span data-stu-id="2ff41-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="2ff41-112">Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor puede ser 19200.</span><span class="sxs-lookup"><span data-stu-id="2ff41-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="2ff41-113">Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamNumber, el miembro **Number** contiene el valor del parámetro específico del medio.</span><span class="sxs-lookup"><span data-stu-id="2ff41-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="2ff41-114">Por ejemplo, el parámetro MAXCONNECTBPS es de tipo ParamNumber y el valor puede ser 19200.</span><span class="sxs-lookup"><span data-stu-id="2ff41-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="2ff41-115">**String**</span><span class="sxs-lookup"><span data-stu-id="2ff41-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="2ff41-116">Si el miembro de **\_ tipo P** de la estructura de [**\_ parámetros de Ras**](ras-parameters-str.md) es ParamString, el miembro de **cadena** contiene el valor del parámetro específico del medio.</span><span class="sxs-lookup"><span data-stu-id="2ff41-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="2ff41-117">**Duración**</span><span class="sxs-lookup"><span data-stu-id="2ff41-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="2ff41-118">Especifica la longitud, en caracteres, de la cadena a la que apunta el miembro de **datos** .</span><span class="sxs-lookup"><span data-stu-id="2ff41-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="2ff41-119">**Data**</span><span class="sxs-lookup"><span data-stu-id="2ff41-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="2ff41-120">Puntero a un búfer que contiene el valor de cadena de un parámetro específico del medio.</span><span class="sxs-lookup"><span data-stu-id="2ff41-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ff41-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ff41-121">Requirements</span></span>



| <span data-ttu-id="2ff41-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff41-122">Requirement</span></span> | <span data-ttu-id="2ff41-123">Value</span><span class="sxs-lookup"><span data-stu-id="2ff41-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff41-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ff41-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff41-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ff41-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ff41-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ff41-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff41-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ff41-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ff41-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2ff41-128">End of client support</span></span><br/>    | <span data-ttu-id="2ff41-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ff41-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="2ff41-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2ff41-130">End of server support</span></span><br/>    | <span data-ttu-id="2ff41-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ff41-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="2ff41-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ff41-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff41-133"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff41-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff41-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ff41-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff41-135">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="2ff41-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="2ff41-136">Unión de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="2ff41-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="2ff41-137">**parámetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="2ff41-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="2ff41-138">**formato de parámetros de RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ff41-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





