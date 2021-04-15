---
title: Método Delete de la clase Win32_TSAccount
description: El método Delete elimina el usuario, el grupo o la cuenta de equipo especificados.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto, clase Win32_TSAccount
- Clase Win32_TSAccount Servicios de Escritorio remoto, método Delete
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422561"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="f8ff1-106">Método Delete de la \_ clase Win32 TSAccount</span><span class="sxs-lookup"><span data-stu-id="f8ff1-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="f8ff1-107">El método **Delete** elimina el usuario, el grupo o la cuenta de equipo especificados.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ff1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8ff1-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="f8ff1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8ff1-109">Parameters</span></span>

<span data-ttu-id="f8ff1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8ff1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8ff1-111">Return value</span></span>

<span data-ttu-id="f8ff1-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f8ff1-113">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ff1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8ff1-114">Remarks</span></span>

<span data-ttu-id="f8ff1-115">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f8ff1-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8ff1-116">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f8ff1-117">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8ff1-118">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f8ff1-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ff1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8ff1-119">Requirements</span></span>



| <span data-ttu-id="f8ff1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ff1-120">Requirement</span></span> | <span data-ttu-id="f8ff1-121">Value</span><span class="sxs-lookup"><span data-stu-id="f8ff1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ff1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8ff1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ff1-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8ff1-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8ff1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8ff1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ff1-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8ff1-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8ff1-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8ff1-126">Namespace</span></span><br/>                | <span data-ttu-id="f8ff1-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f8ff1-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f8ff1-128">MOF</span><span class="sxs-lookup"><span data-stu-id="f8ff1-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8ff1-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff1-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8ff1-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8ff1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8ff1-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff1-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ff1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8ff1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ff1-133">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

