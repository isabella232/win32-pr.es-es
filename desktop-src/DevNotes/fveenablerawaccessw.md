---
description: Habilita o deshabilita la lectura y escritura de sectores de disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907117"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="48c4b-103">FveEnableRawAccessW función)</span><span class="sxs-lookup"><span data-stu-id="48c4b-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="48c4b-104">Habilita o deshabilita la lectura y escritura de sectores de disco.</span><span class="sxs-lookup"><span data-stu-id="48c4b-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48c4b-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="48c4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c4b-107">*VolumeName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48c4b-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c4b-108">Un identificador único para el volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="48c4b-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="48c4b-109">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48c4b-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c4b-110">Si **es true**, permite el acceso al volumen sin formato.</span><span class="sxs-lookup"><span data-stu-id="48c4b-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="48c4b-111">Si es **false**, no se permite el acceso al volumen sin procesar.</span><span class="sxs-lookup"><span data-stu-id="48c4b-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="48c4b-112">Si ya se ha habilitado el acceso sin procesar, pero este valor es **false**, el volumen se vuelve a montar y a validar.</span><span class="sxs-lookup"><span data-stu-id="48c4b-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c4b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48c4b-113">Return value</span></span>

<span data-ttu-id="48c4b-114">Esta función devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="48c4b-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="48c4b-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48c4b-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="48c4b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="48c4b-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48c4b-117"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="48c4b-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="48c4b-118">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="48c4b-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="48c4b-119"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="48c4b-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="48c4b-120">Enabled es **false** y el volumen no estaba ya en modo de acceso sin procesar.</span><span class="sxs-lookup"><span data-stu-id="48c4b-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="48c4b-121"><dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="48c4b-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="48c4b-122">No se puede bloquear el volumen.</span><span class="sxs-lookup"><span data-stu-id="48c4b-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="48c4b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48c4b-123">Requirements</span></span>



| <span data-ttu-id="48c4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c4b-124">Requirement</span></span> | <span data-ttu-id="48c4b-125">Value</span><span class="sxs-lookup"><span data-stu-id="48c4b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48c4b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48c4b-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48c4b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48c4b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48c4b-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="48c4b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48c4b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48c4b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c4b-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c4b-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




