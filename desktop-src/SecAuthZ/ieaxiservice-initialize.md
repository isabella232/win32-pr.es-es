---
description: Comprueba y descarga un objeto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'IeAxiService:: Initialize (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278996"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="45585-103">IeAxiService:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="45585-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="45585-104">El método **Initialize** comprueba y descarga un objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="45585-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="45585-105">Si el objeto cumple los requisitos de la Directiva, este método inicializa un objeto del sistema que instala el objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="45585-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="45585-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45585-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="45585-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45585-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45585-108">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45585-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-109">Identificador de la ventana primaria de la ventana que está intentando instalar el control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="45585-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="45585-110">*dwClientPID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45585-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-111">IDENTIFICADOR de proceso del proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="45585-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="45585-112">*bstrDesktop* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45585-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-113">Escritorio del objeto.</span><span class="sxs-lookup"><span data-stu-id="45585-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="45585-114">*bstrClsID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45585-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-115">IDENTIFICADOR de clase del objeto ActiveX que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="45585-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="45585-116">*bstrURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45585-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-117">Dirección URL del objeto ActiveX que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="45585-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="45585-118">*pbstrNonce* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45585-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-119">Contexto que se puede utilizar para compartir información de estado en llamadas a otros métodos utilizados para comprobar y descargar el objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="45585-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="45585-120">*ppISyncBrokerInterface* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45585-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45585-121">Puntero a la instancia de la interfaz [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala el control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="45585-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45585-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45585-122">Return value</span></span>

<span data-ttu-id="45585-123">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45585-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="45585-124">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="45585-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="45585-125">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45585-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="45585-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="45585-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="45585-127"><dt>**Confianza \_ de E \_ \_ no \_**</dt> es de confianza <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="45585-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="45585-128">El objeto ActiveX no debe estar instalado.</span><span class="sxs-lookup"><span data-stu-id="45585-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="45585-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45585-129">Requirements</span></span>



| <span data-ttu-id="45585-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="45585-130">Requirement</span></span> | <span data-ttu-id="45585-131">Value</span><span class="sxs-lookup"><span data-stu-id="45585-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45585-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45585-132">Minimum supported client</span></span><br/> | <span data-ttu-id="45585-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="45585-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="45585-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45585-134">Minimum supported server</span></span><br/> | <span data-ttu-id="45585-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="45585-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="45585-136">IID</span><span class="sxs-lookup"><span data-stu-id="45585-136">IID</span></span><br/>                      | <span data-ttu-id="45585-137">IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="45585-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="45585-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="45585-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45585-139">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="45585-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




