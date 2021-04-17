---
description: No se admite la función RKeyOpenKeyService.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Función RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687909"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="cd582-103">RKeyOpenKeyService función)</span><span class="sxs-lookup"><span data-stu-id="cd582-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="cd582-104">No se admite la función **RKeyOpenKeyService** .</span><span class="sxs-lookup"><span data-stu-id="cd582-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="cd582-105">**Windows Server 2003:** La función **RKeyOpenKeyService** establece una conexión a un equipo remoto y abre un identificador del servicio de claves.</span><span class="sxs-lookup"><span data-stu-id="cd582-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="cd582-106">Posteriormente, la función [**RKeyPFXInstall**](rkeypfxinstall.md) puede usar el identificador del servicio de claves.</span><span class="sxs-lookup"><span data-stu-id="cd582-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="cd582-107">Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cd582-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd582-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd582-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="cd582-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd582-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd582-110">*pszMachineName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd582-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-111">Puntero largo a una cadena terminada en null que representa el equipo en el que se abrirá el identificador del servicio de claves.</span><span class="sxs-lookup"><span data-stu-id="cd582-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="cd582-112">*OwnerType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd582-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-113">[**KEYSVC \_**](keysvc-type.md) Valor de tipo que representa el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="cd582-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="cd582-114">El único valor admitido es **KeySvcMachine**.</span><span class="sxs-lookup"><span data-stu-id="cd582-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="cd582-115">*pwszOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd582-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cd582-116">Reserved.</span></span> <span data-ttu-id="cd582-117">Establezca este valor en **null**.</span><span class="sxs-lookup"><span data-stu-id="cd582-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd582-118">*pAuthentication* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd582-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-119">Un puntero a un valor **void** que representa la configuración de autenticación.</span><span class="sxs-lookup"><span data-stu-id="cd582-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="cd582-120">Este puntero puede apuntar a un valor de cero o el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="cd582-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="cd582-121">Value</span><span class="sxs-lookup"><span data-stu-id="cd582-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="cd582-122">Significado</span><span class="sxs-lookup"><span data-stu-id="cd582-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="cd582-123"><dt>**RKEYSVC \_ CONECTAR \_ \_ solo con seguridad**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="cd582-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="cd582-124">El cliente requiere autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="cd582-124">The client requires mutual authentication.</span></span> <span data-ttu-id="cd582-125">Si se especifica este valor, se producirá un error de reserva en NTLM.</span><span class="sxs-lookup"><span data-stu-id="cd582-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd582-126">*conservado* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd582-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cd582-127">Reserved.</span></span> <span data-ttu-id="cd582-128">Establezca este valor en **null**.</span><span class="sxs-lookup"><span data-stu-id="cd582-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd582-129">*phKeySvcCli* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd582-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd582-130">Un puntero a un [**\_ identificador de KEYSVCC**](keysvcc-handle.md) que recibe el identificador del servicio de claves abierto.</span><span class="sxs-lookup"><span data-stu-id="cd582-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="cd582-131">Cuando haya terminado de usar el identificador, libere el recurso mediante una llamada a la función [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cd582-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd582-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd582-132">Return value</span></span>

<span data-ttu-id="cd582-133">Si la función se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd582-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="cd582-134">Si se produce un error en la función, el valor devuelto es un **ULong** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="cd582-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd582-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd582-135">Requirements</span></span>



| <span data-ttu-id="cd582-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd582-136">Requirement</span></span> | <span data-ttu-id="cd582-137">Value</span><span class="sxs-lookup"><span data-stu-id="cd582-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd582-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd582-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cd582-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cd582-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="cd582-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd582-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cd582-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd582-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd582-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd582-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd582-143"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd582-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd582-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd582-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd582-145">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="cd582-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="cd582-146">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="cd582-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




