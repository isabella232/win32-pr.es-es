---
title: Método enable de la clase SystemRestore
description: Habilita la supervisión en una unidad determinada.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Habilitar la restauración del sistema de métodos
- Habilitar método Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, enable (método)
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714597"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="99e31-106">Método enable de la clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="99e31-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="99e31-107">Habilita la supervisión en una unidad determinada.</span><span class="sxs-lookup"><span data-stu-id="99e31-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e31-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99e31-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="99e31-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99e31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e31-110">*Unidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="99e31-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e31-111">Unidad que se va a habilitar.</span><span class="sxs-lookup"><span data-stu-id="99e31-111">The drive to be enabled.</span></span> <span data-ttu-id="99e31-112">La cadena de unidad debe tener el formato "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="99e31-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="99e31-113">Si este parámetro es la unidad del sistema o una cadena vacía (""), se supervisan todas las unidades.</span><span class="sxs-lookup"><span data-stu-id="99e31-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e31-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99e31-114">Return value</span></span>

<span data-ttu-id="99e31-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99e31-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="99e31-116">De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.</span><span class="sxs-lookup"><span data-stu-id="99e31-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e31-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99e31-117">Remarks</span></span>

<span data-ttu-id="99e31-118">El método **enable** no espera a que la supervisión se habilite completamente antes de que se devuelva, ya que esto puede tardar unos minutos.</span><span class="sxs-lookup"><span data-stu-id="99e31-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="99e31-119">En su lugar, se devuelve inmediatamente después de iniciar el servicio de restauración del sistema y el controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="99e31-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="99e31-120">Para habilitar Restaurar sistema en una unidad que no es del sistema, primero debe habilitar Restaurar sistema en la unidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="99e31-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="99e31-121">Este método produce un error en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="99e31-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="99e31-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="99e31-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="99e31-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99e31-123">Requirements</span></span>



| <span data-ttu-id="99e31-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e31-124">Requirement</span></span> | <span data-ttu-id="99e31-125">Value</span><span class="sxs-lookup"><span data-stu-id="99e31-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="99e31-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99e31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="99e31-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="99e31-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="99e31-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99e31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="99e31-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="99e31-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="99e31-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99e31-130">Namespace</span></span><br/>                | <span data-ttu-id="99e31-131">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="99e31-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="99e31-132">MOF</span><span class="sxs-lookup"><span data-stu-id="99e31-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99e31-133"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="99e31-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e31-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="99e31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e31-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="99e31-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





