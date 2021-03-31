---
title: Método INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Método DeleteConfig NAP
- Método DeleteConfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801861"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="8f70c-106">INapComponentConfig3::D método eleteConfig</span><span class="sxs-lookup"><span data-stu-id="8f70c-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="8f70c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f70c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8f70c-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **DeleteConfig** para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="8f70c-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="8f70c-109">El identificador se puede reutilizar una vez eliminados los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="8f70c-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f70c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f70c-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="8f70c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f70c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f70c-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="8f70c-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="8f70c-113">Valor que representa los datos de configuración que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8f70c-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f70c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f70c-114">Return value</span></span>

<span data-ttu-id="8f70c-115">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="8f70c-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8f70c-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8f70c-116">Return code</span></span>                                                                                                    | <span data-ttu-id="8f70c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f70c-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f70c-118"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="8f70c-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="8f70c-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f70c-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8f70c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8f70c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="8f70c-121">*ConfigID* es 0 (un valor reservado para la configuración predeterminada).</span><span class="sxs-lookup"><span data-stu-id="8f70c-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="8f70c-122"><dt>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="8f70c-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="8f70c-123">No se encuentra *ConfigID* .</span><span class="sxs-lookup"><span data-stu-id="8f70c-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="8f70c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f70c-124">Requirements</span></span>



| <span data-ttu-id="8f70c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f70c-125">Requirement</span></span> | <span data-ttu-id="8f70c-126">Value</span><span class="sxs-lookup"><span data-stu-id="8f70c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f70c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f70c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8f70c-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8f70c-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f70c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f70c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8f70c-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f70c-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f70c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f70c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f70c-132"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f70c-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f70c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="8f70c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f70c-134"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f70c-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f70c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f70c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f70c-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="8f70c-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





