---
title: IConfigAsfWriter GetCurrentProfile, método
description: El método GetCurrentProfile recupera el perfil definido por la aplicación.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Método GetCurrentProfile formato de Windows Media
- Método GetCurrentProfile formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714397"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="3b094-106">IConfigAsfWriter:: GetCurrentProfile (método)</span><span class="sxs-lookup"><span data-stu-id="3b094-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="3b094-107">El método **GetCurrentProfile** recupera el perfil definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b094-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b094-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b094-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="3b094-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b094-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b094-110">*ppProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3b094-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b094-111">Dirección de un puntero que recibe la interfaz [**IWMProfile**](iwmprofile.md) del perfil definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b094-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b094-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b094-112">Return value</span></span>

<span data-ttu-id="3b094-113">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="3b094-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3b094-114">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b094-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b094-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b094-115">Remarks</span></span>

<span data-ttu-id="3b094-116">Si el método se ejecuta correctamente, el puntero **IWMProfile** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="3b094-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="3b094-117">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="3b094-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b094-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b094-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b094-119">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b094-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 