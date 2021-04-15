---
title: IConfigAsfWriter GetCurrentProfileId, método
description: El método GetCurrentProfileId recupera el identificador de perfil actual. (Solo para perfiles de Windows Media Format 4,0).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Método GetCurrentProfileId formato de Windows Media
- Método GetCurrentProfileId formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695658"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="5339d-107">IConfigAsfWriter:: GetCurrentProfileId (método)</span><span class="sxs-lookup"><span data-stu-id="5339d-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="5339d-108">El método **GetCurrentProfileId** recupera el identificador de perfil actual.</span><span class="sxs-lookup"><span data-stu-id="5339d-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="5339d-109">(Solo para perfiles de Windows Media Format 4,0).</span><span class="sxs-lookup"><span data-stu-id="5339d-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="5339d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5339d-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="5339d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5339d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5339d-112">*pdwProfileId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5339d-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5339d-113">Puntero a una variable de tipo **DWORD** que recibe el ID. de perfil actual.</span><span class="sxs-lookup"><span data-stu-id="5339d-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5339d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5339d-114">Return value</span></span>

<span data-ttu-id="5339d-115">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5339d-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5339d-116">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5339d-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5339d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5339d-117">Remarks</span></span>

<span data-ttu-id="5339d-118">Este método está ahora obsoleto porque supone la versión 4,0 perfiles de SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5339d-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="5339d-119">En su lugar, use [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) o [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) para identificar correctamente un perfil de la versión 7,0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="5339d-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="5339d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5339d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="5339d-121">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5339d-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 