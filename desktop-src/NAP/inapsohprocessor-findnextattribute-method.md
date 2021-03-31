---
title: Método INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Busca la ubicación (índice) del siguiente atributo del tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Método FindNextAttribute NAP
- Método FindNextAttribute NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801316"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="1918b-106">INapSoHProcessor:: FindNextAttribute (método)</span><span class="sxs-lookup"><span data-stu-id="1918b-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="1918b-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1918b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1918b-108">El método **INapSoHProcessor:: FindNextAttribute** busca la ubicación (índice) del siguiente atributo del tipo indicado por *SoHAttributeType*.</span><span class="sxs-lookup"><span data-stu-id="1918b-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="1918b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1918b-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="1918b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1918b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1918b-111">*fromLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1918b-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1918b-112">La ubicación inicial (índice) en el paquete del informe de mantenimiento (SoH) para comenzar la búsqueda de atributos.</span><span class="sxs-lookup"><span data-stu-id="1918b-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="1918b-113">Este valor debe estar en el intervalo de 0 a (**numAttrib** -1), donde **numAttrib** se recupera mediante [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span><span class="sxs-lookup"><span data-stu-id="1918b-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="1918b-114">El paquete SoH utiliza índices de atributos basados en 0.</span><span class="sxs-lookup"><span data-stu-id="1918b-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="1918b-115">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1918b-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1918b-116">Estructura [**SoHAttributeType**](sohattributetype-enum.md) que contiene el tipo de atributo que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="1918b-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="1918b-117">*attributeLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1918b-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1918b-118">Un puntero que contiene la ubicación (índice) en el paquete SoH del primer atributo de tipo *SoHAttributeType* del índice *fromLocation*.</span><span class="sxs-lookup"><span data-stu-id="1918b-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1918b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1918b-119">Return value</span></span>

<span data-ttu-id="1918b-120">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="1918b-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1918b-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1918b-121">Return code</span></span>                                                                                            | <span data-ttu-id="1918b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1918b-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1918b-123"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="1918b-124">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="1918b-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1918b-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="1918b-126">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1918b-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1918b-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="1918b-128">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1918b-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1918b-129"><dt>**\_ \_ no \_ se encontró el archivo de error**</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="1918b-130">No se encontró el atributo.</span><span class="sxs-lookup"><span data-stu-id="1918b-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="1918b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1918b-131">Remarks</span></span>

<span data-ttu-id="1918b-132">El método **FindNextAttribute** busca atributos de tipo *SoHAttributeType* desde el índice especificado por *fromLocation* y superior hasta que se encuentre una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="1918b-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="1918b-133">Si no se encuentra ninguna coincidencia, se devuelve el **archivo de error \_ \_ no \_ encontrado** .</span><span class="sxs-lookup"><span data-stu-id="1918b-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1918b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1918b-134">Requirements</span></span>



| <span data-ttu-id="1918b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1918b-135">Requirement</span></span> | <span data-ttu-id="1918b-136">Value</span><span class="sxs-lookup"><span data-stu-id="1918b-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1918b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1918b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1918b-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1918b-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1918b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1918b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1918b-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1918b-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1918b-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1918b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1918b-142"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="1918b-143">IDL</span><span class="sxs-lookup"><span data-stu-id="1918b-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1918b-144"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="1918b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1918b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1918b-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1918b-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1918b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1918b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1918b-148">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="1918b-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





