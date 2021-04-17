---
title: IConfigAsfWriter ConfigureFilterUsingProfileId, método
description: El método ConfigureFilterUsingProfileId configura el filtro para escribir un archivo ASF con un índice de identificador de perfil (ID.) de la lista de perfiles del sistema. (Solo para perfiles de Windows Media Format 4,0).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Método ConfigureFilterUsingProfileId formato de Windows Media
- Método ConfigureFilterUsingProfileId formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714398"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="70659-107">IConfigAsfWriter:: ConfigureFilterUsingProfileId (método)</span><span class="sxs-lookup"><span data-stu-id="70659-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="70659-108">El método **ConfigureFilterUsingProfileId** configura el filtro para escribir un archivo ASF con un índice de identificador de perfil (ID.) de la lista de perfiles del sistema.</span><span class="sxs-lookup"><span data-stu-id="70659-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="70659-109">(Solo para perfiles de Windows Media Format 4,0).</span><span class="sxs-lookup"><span data-stu-id="70659-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="70659-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70659-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="70659-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70659-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70659-112">*dwProfileId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70659-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70659-113">IDENTIFICADOR de perfil tal y como se define en la versión 4,0 del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="70659-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70659-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70659-114">Return value</span></span>

<span data-ttu-id="70659-115">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70659-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="70659-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="70659-116">Return code</span></span>                                                                                         | <span data-ttu-id="70659-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="70659-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="70659-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="70659-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="70659-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="70659-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="70659-120"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="70659-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="70659-121">El perfil no es válido.</span><span class="sxs-lookup"><span data-stu-id="70659-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="70659-122"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70659-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="70659-123">El gráfico de filtro está detenido.</span><span class="sxs-lookup"><span data-stu-id="70659-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70659-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70659-124">Remarks</span></span>

<span data-ttu-id="70659-125">Este método está ahora obsoleto porque supone la versión 4,0 perfiles de SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="70659-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="70659-126">Para configurar el filtro para la versión 7,0 y los perfiles posteriores, use [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) o [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span><span class="sxs-lookup"><span data-stu-id="70659-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="70659-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="70659-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="70659-128">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70659-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

