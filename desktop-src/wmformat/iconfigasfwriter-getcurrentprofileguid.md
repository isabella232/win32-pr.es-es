---
title: IConfigAsfWriter GetCurrentProfileGuid, método
description: El método GetCurrentProfileGuid recupera el GUID actual del perfil del sistema de Windows Media.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Método GetCurrentProfileGuid formato de Windows Media
- Método GetCurrentProfileGuid formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359304"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="47301-106">IConfigAsfWriter:: GetCurrentProfileGuid (método)</span><span class="sxs-lookup"><span data-stu-id="47301-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="47301-107">El método **GetCurrentProfileGuid** recupera el GUID actual del perfil del sistema de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="47301-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="47301-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47301-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="47301-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47301-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47301-110">*pProfileGuid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="47301-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47301-111">Puntero a una variable de tipo **GUID** que identifica el perfil de sistema actual que usa el filtro.</span><span class="sxs-lookup"><span data-stu-id="47301-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47301-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47301-112">Return value</span></span>

<span data-ttu-id="47301-113">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="47301-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="47301-114">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="47301-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="47301-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47301-115">Remarks</span></span>

<span data-ttu-id="47301-116">Este método no se utiliza con perfiles personalizados (incluidos todos los perfiles que incluyen secuencias que usan los códecs de vídeo y Windows Media Audio) porque todos estos perfiles se crean mediante aplicaciones y no tienen ningún identificador GUID.</span><span class="sxs-lookup"><span data-stu-id="47301-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="47301-117">Si no se carga ningún perfil del sistema, *pProfileGuid* se establecerá en **null**.</span><span class="sxs-lookup"><span data-stu-id="47301-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="47301-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="47301-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="47301-119">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47301-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 