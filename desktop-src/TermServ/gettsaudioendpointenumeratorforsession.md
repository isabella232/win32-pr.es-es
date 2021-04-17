---
title: Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession
description: Devuelve una referencia a un enumerador de punto de conexión de audio para el ID. de sesión especificado.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto función de devolución de llamada GetTSAudioEndpointEnumeratorForSession
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686177"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="d9511-104">Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession</span><span class="sxs-lookup"><span data-stu-id="d9511-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="d9511-105">Devuelve una referencia a un enumerador de punto de conexión de audio para el ID. de sesión especificado.</span><span class="sxs-lookup"><span data-stu-id="d9511-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="d9511-106">Los consumidores de este enumerador de punto de conexión de audio, como MMDevAPI.dll, llaman a esta función para recuperar un enumerador de punto de conexión de audio en una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d9511-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9511-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9511-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="d9511-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9511-109">*SessionID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9511-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9511-110">Identificador de la sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d9511-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="d9511-111">*ppEndpointEnumerator* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d9511-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9511-112">Dirección de un puntero a una interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="d9511-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9511-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9511-113">Return value</span></span>

<span data-ttu-id="d9511-114">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d9511-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9511-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9511-115">Remarks</span></span>

<span data-ttu-id="d9511-116">Esta función no está definida en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d9511-116">This function is not defined in a header file.</span></span> <span data-ttu-id="d9511-117">Debe implementar y exportar esta función en el enumerador de punto de conexión personalizado y usar la firma que se muestra en el bloque de sintaxis anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="d9511-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9511-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9511-118">Requirements</span></span>



| <span data-ttu-id="d9511-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9511-119">Requirement</span></span> | <span data-ttu-id="d9511-120">Value</span><span class="sxs-lookup"><span data-stu-id="d9511-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="d9511-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9511-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9511-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9511-122">None supported</span></span><br/>         |
| <span data-ttu-id="d9511-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9511-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9511-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9511-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9511-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9511-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9511-126">Implementación de un enumerador de punto de conexión de audio personalizado</span><span class="sxs-lookup"><span data-stu-id="d9511-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="d9511-127">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="d9511-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

