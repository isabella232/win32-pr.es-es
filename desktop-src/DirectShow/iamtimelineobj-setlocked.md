---
description: El método SetLocked establece el estado de edición del objeto en bloqueado o desbloqueado.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'IAMTimelineObj:: SetLocked (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680728"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="d825d-103">IAMTimelineObj:: SetLocked (método)</span><span class="sxs-lookup"><span data-stu-id="d825d-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="d825d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d825d-104">\[Deprecated.</span></span> <span data-ttu-id="d825d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d825d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d825d-106">El `SetLocked` método establece el estado de edición del objeto en bloqueado o desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="d825d-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="d825d-107">Un estado bloqueado indica que el objeto no se debe editar; un estado desbloqueado indica que el objeto se puede editar.</span><span class="sxs-lookup"><span data-stu-id="d825d-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="d825d-108">La escala de tiempo no aplica el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d825d-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="d825d-109">La configuración bloqueada solo existe para la comodidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d825d-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="d825d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d825d-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d825d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d825d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d825d-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="d825d-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d825d-113">Valor booleano que especifica el estado de edición del objeto.</span><span class="sxs-lookup"><span data-stu-id="d825d-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="d825d-114">Si es **true**, el objeto está bloqueado y no se debe editar.</span><span class="sxs-lookup"><span data-stu-id="d825d-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="d825d-115">Si es **false**, el objeto se desbloquea y se puede editar.</span><span class="sxs-lookup"><span data-stu-id="d825d-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d825d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d825d-116">Return value</span></span>

<span data-ttu-id="d825d-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d825d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d825d-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d825d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d825d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d825d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d825d-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d825d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d825d-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d825d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d825d-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d825d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d825d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d825d-123">Requirements</span></span>



| <span data-ttu-id="d825d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d825d-124">Requirement</span></span> | <span data-ttu-id="d825d-125">Value</span><span class="sxs-lookup"><span data-stu-id="d825d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d825d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d825d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d825d-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d825d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d825d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d825d-128">Library</span></span><br/> | <dl> <span data-ttu-id="d825d-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d825d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d825d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d825d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d825d-131">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="d825d-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d825d-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d825d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




