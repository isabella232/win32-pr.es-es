---
title: RAS_PARAMETERS estructura (rassapi. h)
description: '\_La función RasAdminPortGetInfo utiliza la estructura de parámetros de ras para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en un servidor RAS.'
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534906"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="d25e7-104">Estructura de parámetros de RAS \_</span><span class="sxs-lookup"><span data-stu-id="d25e7-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="d25e7-105">\[La estructura de **\_ parámetros de Ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="d25e7-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="d25e7-106">La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) utiliza la estructura de **\_ parámetros de Ras** para devolver el nombre y el valor de un parámetro específico del medio asociado a un puerto en un servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="d25e7-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d25e7-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="d25e7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d25e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d25e7-109">**\_Tecla P**</span><span class="sxs-lookup"><span data-stu-id="d25e7-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="d25e7-110">Especifica el nombre de la clave que representa el parámetro específico del medio, como MAXCONNECTBPS.</span><span class="sxs-lookup"><span data-stu-id="d25e7-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="d25e7-111">**\_Tipo P**</span><span class="sxs-lookup"><span data-stu-id="d25e7-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="d25e7-112">Identifica el tipo de datos asociado al parámetro.</span><span class="sxs-lookup"><span data-stu-id="d25e7-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="d25e7-113">Este miembro puede ser uno de los siguientes valores de la enumeración de [**\_ \_ formato**](ras-params-format-str.md) de los parámetros de Ras.</span><span class="sxs-lookup"><span data-stu-id="d25e7-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="d25e7-114">Value</span><span class="sxs-lookup"><span data-stu-id="d25e7-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="d25e7-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d25e7-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="d25e7-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="d25e7-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="d25e7-117">Indica que los datos asociados a la clave son un número.</span><span class="sxs-lookup"><span data-stu-id="d25e7-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="d25e7-118"><dt>**ParamString**</dt></span><span class="sxs-lookup"><span data-stu-id="d25e7-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="d25e7-119">Indica que los datos asociados a la clave son una cadena.</span><span class="sxs-lookup"><span data-stu-id="d25e7-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d25e7-120">**\_Atributos P**</span><span class="sxs-lookup"><span data-stu-id="d25e7-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="d25e7-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d25e7-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d25e7-122">**\_Valor P**</span><span class="sxs-lookup"><span data-stu-id="d25e7-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="d25e7-123">Especifica el valor asociado al parámetro.</span><span class="sxs-lookup"><span data-stu-id="d25e7-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="d25e7-124">Este miembro es una Unión de [**\_ \_ valores de parámetros de Ras**](ras-params-value-str.md) .</span><span class="sxs-lookup"><span data-stu-id="d25e7-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="d25e7-125">Si el miembro de **\_ tipo P** es ParamNumber, el miembro **Number** de la Unión contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="d25e7-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="d25e7-126">Si **el \_ tipo P** es ParamString, el miembro de **cadena** de la Unión contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="d25e7-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d25e7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d25e7-127">Requirements</span></span>



| <span data-ttu-id="d25e7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d25e7-128">Requirement</span></span> | <span data-ttu-id="d25e7-129">Value</span><span class="sxs-lookup"><span data-stu-id="d25e7-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d25e7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25e7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d25e7-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d25e7-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d25e7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25e7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d25e7-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d25e7-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d25e7-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d25e7-134">End of client support</span></span><br/>    | <span data-ttu-id="d25e7-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d25e7-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d25e7-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d25e7-136">End of server support</span></span><br/>    | <span data-ttu-id="d25e7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d25e7-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d25e7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d25e7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d25e7-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d25e7-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d25e7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d25e7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25e7-141">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="d25e7-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d25e7-142">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d25e7-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="d25e7-143">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="d25e7-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="d25e7-144">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="d25e7-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="d25e7-145">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d25e7-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





