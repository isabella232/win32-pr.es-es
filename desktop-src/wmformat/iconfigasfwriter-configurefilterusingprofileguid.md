---
title: IConfigAsfWriter ConfigureFilterUsingProfileGuid, método
description: El método ConfigureFilterUsingProfileGuid configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado. (Desusado).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Método ConfigureFilterUsingProfileGuid formato de Windows Media
- Método ConfigureFilterUsingProfileGuid formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533411"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="4007e-107">IConfigAsfWriter:: ConfigureFilterUsingProfileGuid (método)</span><span class="sxs-lookup"><span data-stu-id="4007e-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="4007e-108">El método **ConfigureFilterUsingProfileGuid** configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado.</span><span class="sxs-lookup"><span data-stu-id="4007e-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="4007e-109">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="4007e-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="4007e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4007e-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="4007e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4007e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4007e-112">*guidProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4007e-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4007e-113">**GUID** que identifica un perfil tal y como se define en el archivo de encabezado del SDK de Windows Media Format Wmsysprf. h.</span><span class="sxs-lookup"><span data-stu-id="4007e-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4007e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4007e-114">Return value</span></span>

<span data-ttu-id="4007e-115">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4007e-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="4007e-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4007e-116">Return code</span></span>                                                                                         | <span data-ttu-id="4007e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4007e-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="4007e-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4007e-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="4007e-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="4007e-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="4007e-120"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="4007e-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="4007e-121">El perfil no es válido.</span><span class="sxs-lookup"><span data-stu-id="4007e-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="4007e-122"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4007e-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="4007e-123">El gráfico de filtro está detenido.</span><span class="sxs-lookup"><span data-stu-id="4007e-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4007e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4007e-124">Remarks</span></span>

<span data-ttu-id="4007e-125">A partir del SDK de Windows Media Format 9 series, no se ha definido ningún perfil del sistema nuevo.</span><span class="sxs-lookup"><span data-stu-id="4007e-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="4007e-126">Con este método solo se pueden usar GUID de Perfil de sistema de la versión 8 (o anterior).</span><span class="sxs-lookup"><span data-stu-id="4007e-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="4007e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4007e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4007e-128">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4007e-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

