---
title: Método INapComponentInfo GetIcon (NapCommon. h)
description: Lo usa el sistema NAP para obtener el icono de un cliente de mantenimiento.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Método GetIcon NAP
- Método GetIcon NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997007"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="dd3b2-106">INapComponentInfo:: GetIcon (método)</span><span class="sxs-lookup"><span data-stu-id="dd3b2-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="dd3b2-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="dd3b2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dd3b2-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetIcon** para obtener el icono de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3b2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd3b2-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="dd3b2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd3b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd3b2-111">*dllFilePath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dd3b2-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd3b2-112">Un puntero a un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) usado para devolver la ruta de acceso del archivo DLL que contiene el icono.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="dd3b2-113">*iconResourceId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dd3b2-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd3b2-114">Puntero al valor que se usa para devolver el identificador de recurso del icono que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd3b2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd3b2-115">Return value</span></span>

<span data-ttu-id="dd3b2-116">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="dd3b2-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dd3b2-117">Return code</span></span>                                                                                     | <span data-ttu-id="dd3b2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd3b2-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd3b2-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="dd3b2-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="dd3b2-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="dd3b2-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="dd3b2-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="dd3b2-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dd3b2-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd3b2-125">Remarks</span></span>

<span data-ttu-id="dd3b2-126">Los iconos deben localizarse según el identificador de idioma del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="dd3b2-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3b2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd3b2-127">Requirements</span></span>



| <span data-ttu-id="dd3b2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd3b2-128">Requirement</span></span> | <span data-ttu-id="dd3b2-129">Value</span><span class="sxs-lookup"><span data-stu-id="dd3b2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3b2-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3b2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3b2-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3b2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd3b2-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3b2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3b2-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3b2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd3b2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd3b2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3b2-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd3b2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="dd3b2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd3b2-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3b2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd3b2-138">See also</span></span>

<dl> <span data-ttu-id="dd3b2-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="dd3b2-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="dd3b2-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="dd3b2-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





