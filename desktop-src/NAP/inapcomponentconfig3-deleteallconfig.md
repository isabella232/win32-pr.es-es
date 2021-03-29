---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Método DeleteAllConfig NAP
- Método DeleteAllConfig NAP, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905126"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="44fb8-106">INapComponentConfig3::D método eleteAllConfig</span><span class="sxs-lookup"><span data-stu-id="44fb8-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="44fb8-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="44fb8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="44fb8-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **DeleteAllConfig** para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="44fb8-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="44fb8-109">Se deben eliminar todos los datos de configuración excepto la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="44fb8-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fb8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44fb8-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="44fb8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44fb8-111">Parameters</span></span>

<span data-ttu-id="44fb8-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="44fb8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44fb8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44fb8-113">Return value</span></span>

<span data-ttu-id="44fb8-114">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="44fb8-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="44fb8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="44fb8-115">Return code</span></span>                                                                           | <span data-ttu-id="44fb8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="44fb8-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="44fb8-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="44fb8-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="44fb8-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="44fb8-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="44fb8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44fb8-119">Requirements</span></span>



| <span data-ttu-id="44fb8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="44fb8-120">Requirement</span></span> | <span data-ttu-id="44fb8-121">Value</span><span class="sxs-lookup"><span data-stu-id="44fb8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44fb8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44fb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44fb8-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44fb8-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="44fb8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44fb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44fb8-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44fb8-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44fb8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44fb8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44fb8-127"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44fb8-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="44fb8-128">IDL</span><span class="sxs-lookup"><span data-stu-id="44fb8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44fb8-129"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44fb8-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fb8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="44fb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fb8-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="44fb8-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





