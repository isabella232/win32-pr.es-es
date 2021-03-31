---
description: Instala el objeto ActiveX especificado.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'IeAxiSystemInstaller:: InitializeSystemInstaller (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912430"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="841e6-103">IeAxiSystemInstaller:: InitializeSystemInstaller (método)</span><span class="sxs-lookup"><span data-stu-id="841e6-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="841e6-104">El método **InitializeSystemInstaller** instala el objeto ActiveX especificado.</span><span class="sxs-lookup"><span data-stu-id="841e6-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="841e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="841e6-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="841e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="841e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841e6-107">*bstrUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e6-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e6-108">Dirección URL del objeto ActiveX que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="841e6-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="841e6-109">*dwClientPID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e6-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e6-110">IDENTIFICADOR de proceso del proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="841e6-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="841e6-111">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e6-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e6-112">Puntero a una instancia de la interfaz [**IeAxiServiceCallback**](ieaxiservicecallback.md) que comprueba si se permite instalar el objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="841e6-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="841e6-113">*pbstrNonce* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="841e6-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="841e6-114">Contexto que se puede utilizar para compartir información de estado en llamadas a otros métodos utilizados para comprobar y descargar el objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="841e6-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841e6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="841e6-115">Return value</span></span>

<span data-ttu-id="841e6-116">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="841e6-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="841e6-117">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="841e6-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="841e6-118">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="841e6-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="841e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841e6-119">Requirements</span></span>



| <span data-ttu-id="841e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="841e6-120">Requirement</span></span> | <span data-ttu-id="841e6-121">Value</span><span class="sxs-lookup"><span data-stu-id="841e6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841e6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="841e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="841e6-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="841e6-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="841e6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="841e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="841e6-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="841e6-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="841e6-126">IID</span><span class="sxs-lookup"><span data-stu-id="841e6-126">IID</span></span><br/>                      | <span data-ttu-id="841e6-127">IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="841e6-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="841e6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="841e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841e6-129">**IeAxiSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="841e6-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

