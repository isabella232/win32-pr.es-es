---
title: Método INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Método GetConfigFromID NAP
- Método GetConfigFromID NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801855"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="653ca-106">INapComponentConfig3:: GetConfigFromID (método)</span><span class="sxs-lookup"><span data-stu-id="653ca-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="653ca-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="653ca-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="653ca-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **GetConfigFromID** para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="653ca-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="653ca-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="653ca-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="653ca-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="653ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="653ca-111">*configID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="653ca-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="653ca-112">Valor que representa la configuración.</span><span class="sxs-lookup"><span data-stu-id="653ca-112">A value that represents the configuration.</span></span> <span data-ttu-id="653ca-113">Si *ConfigID* es **0**, el SHV debe devolver los datos de configuración predeterminados *de los datos.*</span><span class="sxs-lookup"><span data-stu-id="653ca-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="653ca-114">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="653ca-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="653ca-115">Tamaño, en bytes, de los datos de configuración devueltos en *outdata*.</span><span class="sxs-lookup"><span data-stu-id="653ca-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="653ca-116">*outdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="653ca-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="653ca-117">En la devolución, una matriz de BYTEs que contiene los datos de configuración representados por *ConfigID*.</span><span class="sxs-lookup"><span data-stu-id="653ca-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="653ca-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="653ca-118">Return value</span></span>

<span data-ttu-id="653ca-119">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="653ca-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="653ca-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="653ca-120">Return code</span></span>                                                                                                    | <span data-ttu-id="653ca-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="653ca-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="653ca-122"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="653ca-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="653ca-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="653ca-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="653ca-124"><dt>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**</dt></span><span class="sxs-lookup"><span data-stu-id="653ca-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="653ca-125">No se encuentra *ConfigID* .</span><span class="sxs-lookup"><span data-stu-id="653ca-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="653ca-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="653ca-126">Remarks</span></span>

<span data-ttu-id="653ca-127">El método [**documento newconfig**](inapcomponentconfig3-newconfig.md) debe usarse para asignar los datos de configuración de *ConfigID* antes de que se pueda llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="653ca-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="653ca-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653ca-128">Requirements</span></span>



| <span data-ttu-id="653ca-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="653ca-129">Requirement</span></span> | <span data-ttu-id="653ca-130">Value</span><span class="sxs-lookup"><span data-stu-id="653ca-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="653ca-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653ca-131">Minimum supported client</span></span><br/> | <span data-ttu-id="653ca-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="653ca-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="653ca-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653ca-133">Minimum supported server</span></span><br/> | <span data-ttu-id="653ca-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="653ca-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="653ca-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="653ca-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="653ca-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="653ca-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="653ca-137">IDL</span><span class="sxs-lookup"><span data-stu-id="653ca-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="653ca-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="653ca-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653ca-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="653ca-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653ca-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="653ca-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





