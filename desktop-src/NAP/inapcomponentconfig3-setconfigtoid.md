---
title: Método INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Los validadores de mantenimiento del sistema (SHV) implementan para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Método SetConfigToID NAP
- Método SetConfigToID NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666086"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="2bf08-106">INapComponentConfig3:: SetConfigToID (método)</span><span class="sxs-lookup"><span data-stu-id="2bf08-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="2bf08-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2bf08-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2bf08-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **SetConfigToID** para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="2bf08-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf08-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bf08-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="2bf08-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bf08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf08-111">*configID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bf08-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf08-112">Valor que representa la configuración.</span><span class="sxs-lookup"><span data-stu-id="2bf08-112">A value that represents the configuration.</span></span> <span data-ttu-id="2bf08-113">El servicio del servidor de directivas de redes (NPS) asigna *ConfigID* y es único en el SHV.</span><span class="sxs-lookup"><span data-stu-id="2bf08-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="2bf08-114">Si *ConfigID* es 0, se establece la configuración predeterminada del SHV.</span><span class="sxs-lookup"><span data-stu-id="2bf08-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="2bf08-115">*recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2bf08-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf08-116">Tamaño, en bytes, de los datos de configuración de los *datos*.</span><span class="sxs-lookup"><span data-stu-id="2bf08-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="2bf08-117">*datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2bf08-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf08-118">En la entrada, una matriz de BYTEs que contiene los datos de configuración establecidos en *ConfigID*.</span><span class="sxs-lookup"><span data-stu-id="2bf08-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf08-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bf08-119">Return value</span></span>

<span data-ttu-id="2bf08-120">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="2bf08-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="2bf08-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2bf08-121">Return code</span></span>                                                                                                    | <span data-ttu-id="2bf08-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bf08-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2bf08-123"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="2bf08-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="2bf08-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2bf08-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="2bf08-125"><dt>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="2bf08-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="2bf08-126">No se encuentra *ConfigID* .</span><span class="sxs-lookup"><span data-stu-id="2bf08-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2bf08-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bf08-127">Remarks</span></span>

<span data-ttu-id="2bf08-128">El método [**documento newconfig**](inapcomponentconfig3-newconfig.md) debe usarse para asignar los datos de configuración de *ConfigID* antes de que se pueda llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="2bf08-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf08-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf08-129">Requirements</span></span>



| <span data-ttu-id="2bf08-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf08-130">Requirement</span></span> | <span data-ttu-id="2bf08-131">Value</span><span class="sxs-lookup"><span data-stu-id="2bf08-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf08-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf08-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf08-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2bf08-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2bf08-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf08-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf08-135">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bf08-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bf08-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bf08-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf08-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bf08-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bf08-138">IDL</span><span class="sxs-lookup"><span data-stu-id="2bf08-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bf08-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bf08-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf08-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bf08-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf08-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="2bf08-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





