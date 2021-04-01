---
title: Método INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) según sea necesario para cargar la configuración de un equipo remoto o local en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Método InvokeUIFromConfigBlob NAP
- Método InvokeUIFromConfigBlob NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905127"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="2f04c-106">INapComponentConfig2:: InvokeUIFromConfigBlob (método)</span><span class="sxs-lookup"><span data-stu-id="2f04c-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="2f04c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2f04c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2f04c-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **InvokeUIFromConfigBlob** según sea necesario para cargar la configuración de un equipo remoto o local en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="2f04c-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="2f04c-109">El componente de configuración debe admitir el uso de [**INapComponentConfig**](inapcomponentconfig.md) a través de DCOM.</span><span class="sxs-lookup"><span data-stu-id="2f04c-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f04c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f04c-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="2f04c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f04c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f04c-112">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-113">Identificador de la ventana primaria o propietaria.</span><span class="sxs-lookup"><span data-stu-id="2f04c-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="2f04c-114">Se debe proporcionar un identificador de ventana válido.</span><span class="sxs-lookup"><span data-stu-id="2f04c-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="2f04c-115">*inbCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-116">Tamaño, en bytes, de los *datos*.</span><span class="sxs-lookup"><span data-stu-id="2f04c-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="2f04c-117">*datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-118">Puntero a un búfer que almacena los datos de configuración iniciales.</span><span class="sxs-lookup"><span data-stu-id="2f04c-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="2f04c-119">Estos datos se exportan desde el equipo remoto o local.</span><span class="sxs-lookup"><span data-stu-id="2f04c-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="2f04c-120">*outbCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-121">Tamaño de los *datos*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2f04c-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="2f04c-122">*outdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-123">Un puntero a un búfer que almacena los datos de configuración modificados por la interfaz de usuario de la configuración de SHV.</span><span class="sxs-lookup"><span data-stu-id="2f04c-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="2f04c-124">Estos datos son importados por el equipo remoto o local.</span><span class="sxs-lookup"><span data-stu-id="2f04c-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="2f04c-125">*fConfigChanged* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f04c-126">Un puntero a un valor **booleano** que se establece en **true** si se cambió la configuración durante la operación de la interfaz de usuario y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2f04c-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f04c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f04c-127">Return value</span></span>

<span data-ttu-id="2f04c-128">Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="2f04c-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f04c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f04c-129">Remarks</span></span>

<span data-ttu-id="2f04c-130">Si se usa para un equipo local, esta función se puede usar para la configuración de SHV por directiva.</span><span class="sxs-lookup"><span data-stu-id="2f04c-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="2f04c-131">Proporciona una manera de invocar una interfaz de usuario de SHV y editar una configuración de SHV existente.</span><span class="sxs-lookup"><span data-stu-id="2f04c-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f04c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f04c-132">Requirements</span></span>



| <span data-ttu-id="2f04c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f04c-133">Requirement</span></span> | <span data-ttu-id="2f04c-134">Value</span><span class="sxs-lookup"><span data-stu-id="2f04c-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f04c-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f04c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f04c-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2f04c-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2f04c-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f04c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f04c-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f04c-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f04c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f04c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f04c-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f04c-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f04c-141">IDL</span><span class="sxs-lookup"><span data-stu-id="2f04c-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f04c-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f04c-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f04c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f04c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f04c-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="2f04c-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





