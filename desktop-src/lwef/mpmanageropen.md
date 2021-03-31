---
title: Función MpManagerOpen (MpClient. h)
description: Establece una conexión con el administrador de protección contra malware en el equipo local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Función MpManagerOpen características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803536"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="29277-104">MpManagerOpen función)</span><span class="sxs-lookup"><span data-stu-id="29277-104">MpManagerOpen function</span></span>

<span data-ttu-id="29277-105">Establece una conexión con el administrador de protección contra malware en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="29277-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="29277-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29277-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="29277-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29277-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29277-108">*dwReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29277-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29277-109">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="29277-109">Type: **DWORD**</span></span>

<span data-ttu-id="29277-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="29277-110">Reserved for future use.</span></span> <span data-ttu-id="29277-111">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="29277-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="29277-112">*phMpHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29277-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29277-113">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="29277-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="29277-114">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="29277-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="29277-115">Este identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="29277-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29277-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29277-116">Return value</span></span>

<span data-ttu-id="29277-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29277-117">Type: **HRESULT**</span></span>

<span data-ttu-id="29277-118">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="29277-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="29277-119">Se garantiza que esta llamada de función se realiza correctamente aunque no se esté ejecutando un servicio antimalware.</span><span class="sxs-lookup"><span data-stu-id="29277-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="29277-120">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="29277-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="29277-121">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="29277-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="29277-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29277-122">Requirements</span></span>



| <span data-ttu-id="29277-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="29277-123">Requirement</span></span> | <span data-ttu-id="29277-124">Value</span><span class="sxs-lookup"><span data-stu-id="29277-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29277-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29277-125">Minimum supported client</span></span><br/> | <span data-ttu-id="29277-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="29277-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="29277-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29277-127">Minimum supported server</span></span><br/> | <span data-ttu-id="29277-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="29277-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29277-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29277-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="29277-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="29277-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="29277-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29277-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29277-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29277-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29277-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="29277-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29277-134">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="29277-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="29277-135">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="29277-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





