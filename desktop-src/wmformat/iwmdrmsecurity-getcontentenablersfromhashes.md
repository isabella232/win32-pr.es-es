---
title: Método IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: El método GetContentEnablersFromHashes recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Método GetContentEnablersFromHashes formato de Windows Media
- Método GetContentEnablersFromHashes formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649577"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="ac18f-106">IWMDRMSecurity:: GetContentEnablersFromHashes (método)</span><span class="sxs-lookup"><span data-stu-id="ac18f-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="ac18f-107">El método **GetContentEnablersFromHashes** recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.</span><span class="sxs-lookup"><span data-stu-id="ac18f-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac18f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac18f-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="ac18f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac18f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac18f-110">*rgpbCertHashes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac18f-111">Matriz de hash de certificado para el que se van a obtener habilitadores de contenido.</span><span class="sxs-lookup"><span data-stu-id="ac18f-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="ac18f-112">*cCerts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac18f-113">Número de certificados para los que se van a recuperar los habilitadores de contenido.</span><span class="sxs-lookup"><span data-stu-id="ac18f-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="ac18f-114">Es el número de elementos de la matriz *rgpbCertHashes* .</span><span class="sxs-lookup"><span data-stu-id="ac18f-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="ac18f-115">*hResultHint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac18f-116">Valor devuelto recibido de la operación que produjo un error debido a un certificado revocado.</span><span class="sxs-lookup"><span data-stu-id="ac18f-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="ac18f-117">Si no llama a en respuesta a una llamada al método con errores, establezca en es \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ac18f-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="ac18f-118">*prgContentEnablers* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac18f-119">Matriz que recibe las direcciones de las interfaces **IMFContentEnabler** recién creadas.</span><span class="sxs-lookup"><span data-stu-id="ac18f-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="ac18f-120">Establezca en **null** para obtener el número de habilitadores de contenido en el parámetro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="ac18f-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ac18f-121">*pcContentEnablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac18f-122">Número de elementos de la matriz *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="ac18f-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="ac18f-123">Si *prgContentEnablers* es **null**, este valor se establece en el número de habilitadores de contenido necesarios en la salida.</span><span class="sxs-lookup"><span data-stu-id="ac18f-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac18f-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac18f-124">Return value</span></span>

<span data-ttu-id="ac18f-125">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ac18f-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac18f-126">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ac18f-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac18f-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ac18f-127">Return code</span></span>                                                                          | <span data-ttu-id="ac18f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac18f-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac18f-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ac18f-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ac18f-130">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ac18f-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac18f-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac18f-131">Remarks</span></span>

<span data-ttu-id="ac18f-132">Si usa la interfaz **IMFContentEnabler** para renovar los componentes revocados, debe aclarar el proceso al usuario.</span><span class="sxs-lookup"><span data-stu-id="ac18f-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="ac18f-133">Esta Aclaración debe realizarse porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac18f-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="ac18f-134">Cuando se llama a **IMFContentEnabler:: AutomaticEnable**, el habilitador de contenido inicia el explorador predeterminado con la dirección del servicio de actualización en el sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac18f-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="ac18f-135">Un identificador único que identifica el componente revocado se envía al servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="ac18f-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="ac18f-136">A continuación, el servicio redirige el explorador a una página web desde la que el usuario puede descargar e instalar la nueva versión del componente revocado.</span><span class="sxs-lookup"><span data-stu-id="ac18f-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac18f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac18f-137">Requirements</span></span>



| <span data-ttu-id="ac18f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac18f-138">Requirement</span></span> | <span data-ttu-id="ac18f-139">Value</span><span class="sxs-lookup"><span data-stu-id="ac18f-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac18f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac18f-140">Header</span></span><br/>  | <dl> <span data-ttu-id="ac18f-141"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac18f-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac18f-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac18f-142">Library</span></span><br/> | <dl> <span data-ttu-id="ac18f-143"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac18f-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac18f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac18f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac18f-145">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="ac18f-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





