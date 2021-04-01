---
title: Método INapComponentConfig3 documento newconfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Método documento newconfig NAP
- Método documento newconfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método documento newconfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150102"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="5caa1-106">INapComponentConfig3:: documento newconfig (método)</span><span class="sxs-lookup"><span data-stu-id="5caa1-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="5caa1-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5caa1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5caa1-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **documento newconfig** para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="5caa1-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="5caa1-109">Cuando se llama a esta función, un SHV debe asignar nuevos datos de configuración y rellenarlos con una copia de los datos de configuración predeterminados.</span><span class="sxs-lookup"><span data-stu-id="5caa1-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5caa1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5caa1-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="5caa1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5caa1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5caa1-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="5caa1-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="5caa1-113">Valor que representa la configuración.</span><span class="sxs-lookup"><span data-stu-id="5caa1-113">A value that represents the configuration.</span></span> <span data-ttu-id="5caa1-114">El servicio del servidor de directivas de redes (NPS) asigna *ConfigID* y es único en el SHV.</span><span class="sxs-lookup"><span data-stu-id="5caa1-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5caa1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5caa1-115">Return value</span></span>

<span data-ttu-id="5caa1-116">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="5caa1-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="5caa1-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5caa1-117">Return code</span></span>                                                                                                 | <span data-ttu-id="5caa1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5caa1-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5caa1-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="5caa1-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5caa1-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="5caa1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="5caa1-122">*ConfigID* es 0 (un valor reservado para la configuración predeterminada).</span><span class="sxs-lookup"><span data-stu-id="5caa1-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="5caa1-123"><dt>**\_existe la \_ configuración de SHV E \_ NAP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="5caa1-124">*ConfigID* ya existe.</span><span class="sxs-lookup"><span data-stu-id="5caa1-124">*ConfigID* already exists.</span></span> <span data-ttu-id="5caa1-125">La lista de identificadores conocidos para NPS es diferente del SHV.</span><span class="sxs-lookup"><span data-stu-id="5caa1-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5caa1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5caa1-126">Remarks</span></span>

<span data-ttu-id="5caa1-127">Una vez que **documento newconfig** crea la nueva configuración, se deben usar los métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)y [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) para modificar la configuración según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5caa1-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5caa1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5caa1-128">Requirements</span></span>



| <span data-ttu-id="5caa1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5caa1-129">Requirement</span></span> | <span data-ttu-id="5caa1-130">Value</span><span class="sxs-lookup"><span data-stu-id="5caa1-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5caa1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5caa1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5caa1-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5caa1-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5caa1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5caa1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5caa1-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5caa1-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5caa1-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5caa1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5caa1-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="5caa1-137">IDL</span><span class="sxs-lookup"><span data-stu-id="5caa1-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5caa1-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5caa1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5caa1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5caa1-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="5caa1-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





