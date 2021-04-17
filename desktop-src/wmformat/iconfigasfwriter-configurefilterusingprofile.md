---
title: IConfigAsfWriter ConfigureFilterUsingProfile, método
description: El método ConfigureFilterUsingProfile es la forma recomendada para establecer un perfil. Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Método ConfigureFilterUsingProfile formato de Windows Media
- Método ConfigureFilterUsingProfile formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705017"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="62080-107">IConfigAsfWriter:: ConfigureFilterUsingProfile (método)</span><span class="sxs-lookup"><span data-stu-id="62080-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="62080-108">El método **ConfigureFilterUsingProfile** es la forma recomendada para establecer un perfil.</span><span class="sxs-lookup"><span data-stu-id="62080-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="62080-109">Configura el filtro para escribir un archivo ASF basado en el perfil definido por la aplicación especificado.</span><span class="sxs-lookup"><span data-stu-id="62080-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="62080-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62080-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="62080-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62080-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62080-112">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62080-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62080-113">Puntero a la interfaz [**IWMProfile**](iwmprofile.md) en el perfil definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="62080-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62080-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62080-114">Return value</span></span>

<span data-ttu-id="62080-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="62080-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62080-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="62080-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62080-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="62080-117">Return code</span></span>                                                                                         | <span data-ttu-id="62080-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="62080-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="62080-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="62080-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="62080-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="62080-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="62080-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="62080-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="62080-122">El puntero de la interfaz **IWMProfile** no es válido.</span><span class="sxs-lookup"><span data-stu-id="62080-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="62080-123"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62080-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="62080-124">El gráfico está detenido.</span><span class="sxs-lookup"><span data-stu-id="62080-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="62080-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62080-125">Remarks</span></span>

<span data-ttu-id="62080-126">Si se realiza correctamente, este método hará que se envíe un evento de **\_ \_ cambio de gráfico de EC** a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="62080-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="62080-127">Use este método para configurar el escritor con un perfil de la serie de Windows Media 9 personalizado que haya creado (o cargado desde un archivo. prx existente) mediante los métodos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="62080-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="62080-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="62080-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="62080-129">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62080-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

