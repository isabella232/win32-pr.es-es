---
title: Método Disable de la clase SystemRestore
description: Deshabilita la supervisión en una unidad determinada.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Deshabilitar método Restaurar sistema
- Deshabilitar método Restaurar sistema, clase SystemRestore
- Clase SystemRestore Restaurar sistema, deshabilitar método
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150413"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="25d7f-106">Método Disable de la clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="25d7f-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="25d7f-107">Deshabilita la supervisión en una unidad determinada.</span><span class="sxs-lookup"><span data-stu-id="25d7f-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d7f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25d7f-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="25d7f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25d7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d7f-110">*Unidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="25d7f-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25d7f-111">Unidad que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="25d7f-111">The drive to be disabled.</span></span> <span data-ttu-id="25d7f-112">La cadena de unidad debe tener el formato "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="25d7f-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="25d7f-113">Si este parámetro es la unidad del sistema o una cadena vacía (""), no se supervisan las unidades.</span><span class="sxs-lookup"><span data-stu-id="25d7f-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25d7f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25d7f-114">Return value</span></span>

<span data-ttu-id="25d7f-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25d7f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="25d7f-116">De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.</span><span class="sxs-lookup"><span data-stu-id="25d7f-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="25d7f-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25d7f-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="25d7f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25d7f-118">Requirements</span></span>



| <span data-ttu-id="25d7f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d7f-119">Requirement</span></span> | <span data-ttu-id="25d7f-120">Value</span><span class="sxs-lookup"><span data-stu-id="25d7f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="25d7f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d7f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25d7f-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="25d7f-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="25d7f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25d7f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25d7f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25d7f-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="25d7f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25d7f-125">Namespace</span></span><br/>                | <span data-ttu-id="25d7f-126">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="25d7f-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="25d7f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="25d7f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25d7f-128"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="25d7f-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25d7f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="25d7f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d7f-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="25d7f-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





