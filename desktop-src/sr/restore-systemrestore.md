---
title: Método restore de la clase SystemRestore
description: Inicia una restauración del sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore Method Restaurar sistema
- Restore Method System Restore, clase SystemRestore
- Clase SystemRestore System Restore, método restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801382"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="a8613-106">Método restore de la clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="a8613-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="a8613-107">Inicia una restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="a8613-107">Initiates a system restore.</span></span> <span data-ttu-id="a8613-108">El autor de la llamada debe forzar el reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a8613-108">The caller must force a system reboot.</span></span> <span data-ttu-id="a8613-109">La restauración real se produce durante el reinicio.</span><span class="sxs-lookup"><span data-stu-id="a8613-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8613-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8613-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="a8613-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8613-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8613-112">*SequenceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8613-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8613-113">Número de secuencia del punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="a8613-113">The sequence number of the restore point.</span></span> <span data-ttu-id="a8613-114">Para determinar el número de secuencia de un punto de restauración específico, enumere todos los puntos de restauración en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a8613-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8613-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8613-115">Return value</span></span>

<span data-ttu-id="a8613-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8613-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a8613-117">De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.</span><span class="sxs-lookup"><span data-stu-id="a8613-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="a8613-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8613-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="a8613-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8613-119">Requirements</span></span>



| <span data-ttu-id="a8613-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8613-120">Requirement</span></span> | <span data-ttu-id="a8613-121">Value</span><span class="sxs-lookup"><span data-stu-id="a8613-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8613-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8613-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8613-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a8613-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a8613-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8613-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8613-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a8613-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="a8613-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8613-126">Namespace</span></span><br/>                | <span data-ttu-id="a8613-127">Raíz \\ \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="a8613-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="a8613-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a8613-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8613-129"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8613-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8613-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8613-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8613-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="a8613-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





