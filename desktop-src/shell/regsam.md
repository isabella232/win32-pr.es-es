---
description: Un tipo de datos que se usa para especificar los atributos de acceso de seguridad en el registro.
title: REGSAM (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987606"
---
# <a name="regsam"></a><span data-ttu-id="3cd67-103">REGSAM</span><span class="sxs-lookup"><span data-stu-id="3cd67-103">REGSAM</span></span>

<span data-ttu-id="3cd67-104">Un tipo de datos que se usa para especificar los atributos de acceso de seguridad en el registro.</span><span class="sxs-lookup"><span data-stu-id="3cd67-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="3cd67-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3cd67-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="3cd67-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cd67-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="3cd67-107"><dt>**acceso de clave \_ \_ a todo**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="3cd67-108">Combinación de \* \* \* \* valor de consulta de clave \* \* \* \*, \* \* \* \* subclaves de \_ \_ \_ enumeración de clave \_ \* \* \* \* \_ , \* \* \* \* notificación de clave \_ \* \* \* \*, \* \* \* \* clave de \_ creación \_ \_ \_ \_ \_ \_ de clave \* \* \* \* \* \* \* \* \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="3cd67-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="3cd67-109"><dt>**\_vínculo de creación de clave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="3cd67-110">Permiso para crear un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="3cd67-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="3cd67-111"><dt>**subclave de creación de clave \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="3cd67-112">Permiso para crear subclaves.</span><span class="sxs-lookup"><span data-stu-id="3cd67-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="3cd67-113"><dt>**subclaves de \_ enumeración de clave \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="3cd67-114">Permiso para enumerar las subclaves.</span><span class="sxs-lookup"><span data-stu-id="3cd67-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="3cd67-115"><dt>**ejecución de clave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="3cd67-116">Permiso de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="3cd67-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="3cd67-117"><dt>**notificación de clave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="3cd67-118">Permiso para la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="3cd67-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="3cd67-119"><dt>**\_valor de consulta de clave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="3cd67-120">Permiso para consultar los datos de subclaves.</span><span class="sxs-lookup"><span data-stu-id="3cd67-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="3cd67-121"><dt>**lectura de clave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="3cd67-122">Combinación de \* \* \* \* valor de consulta de clave \* \* \* \*, \* \* \* \* subclaves de \_ \_ enumeración de claves \* \* \* \* y \* \* \* \* el \_ \_ \_ \_ acceso a la clave.</span><span class="sxs-lookup"><span data-stu-id="3cd67-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="3cd67-123"><dt>**\_valor del conjunto de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="3cd67-124">Permiso para establecer los datos de la subclave.</span><span class="sxs-lookup"><span data-stu-id="3cd67-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="3cd67-125"><dt>**escritura de claves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="3cd67-126">Combinación de \* \* \* \* valor del conjunto de claves \* \* \* \* \* \_ \_ y \* \* \* \* acceso de clave de \_ creación de \_ clave \_</span><span class="sxs-lookup"><span data-stu-id="3cd67-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="3cd67-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cd67-127">Remarks</span></span>

<span data-ttu-id="3cd67-128">Un valor de **REGSAM** puede ser uno o varios de los valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="3cd67-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd67-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cd67-129">Requirements</span></span>



| <span data-ttu-id="3cd67-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cd67-130">Requirement</span></span> | <span data-ttu-id="3cd67-131">Value</span><span class="sxs-lookup"><span data-stu-id="3cd67-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd67-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cd67-132">Header</span></span><br/> | <dl> <span data-ttu-id="3cd67-133"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd67-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




