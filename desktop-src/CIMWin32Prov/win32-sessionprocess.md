---
description: La \_ clase WMI SessionProcess Association de Win32 representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659355"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="0c107-103">\_Clase Win32 SessionProcess</span><span class="sxs-lookup"><span data-stu-id="0c107-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="0c107-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SessionProcess** Association de Win32 representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.</span><span class="sxs-lookup"><span data-stu-id="0c107-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="0c107-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0c107-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0c107-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0c107-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c107-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c107-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0c107-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c107-108">Members</span></span>

<span data-ttu-id="0c107-109">La **clase \_ SessionProcess de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c107-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="0c107-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c107-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c107-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c107-111">Properties</span></span>

<span data-ttu-id="0c107-112">La **clase \_ SessionProcess de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c107-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c107-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0c107-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c107-114">Tipo de datos: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="0c107-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="0c107-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c107-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c107-116">Calificadores: [**invalidar**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0c107-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0c107-117">[**\_ LogonSession de Win32**](win32-logonsessionmappeddisk.md) que representa la sesión relacionada con el proceso.</span><span class="sxs-lookup"><span data-stu-id="0c107-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="0c107-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0c107-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c107-119">Tipo de datos **: \_ proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="0c107-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="0c107-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c107-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c107-121">Calificadores: [**invalidar**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0c107-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0c107-122">[**\_ Proceso de Win32**](win32-processor.md) que representa el proceso asociado a la sesión.</span><span class="sxs-lookup"><span data-stu-id="0c107-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c107-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c107-123">Remarks</span></span>

<span data-ttu-id="0c107-124">**Win32 \_ SessionProcess** devuelve todas las sesiones para el administrador cuando se inicia sesión con privilegios elevados o cuando se ejecuta de forma remota.</span><span class="sxs-lookup"><span data-stu-id="0c107-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="0c107-125">Se trata de una extensión del comportamiento de la clase.</span><span class="sxs-lookup"><span data-stu-id="0c107-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c107-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c107-126">Requirements</span></span>



| <span data-ttu-id="0c107-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c107-127">Requirement</span></span> | <span data-ttu-id="0c107-128">Value</span><span class="sxs-lookup"><span data-stu-id="0c107-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c107-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c107-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c107-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c107-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c107-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c107-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c107-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c107-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c107-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c107-133">Namespace</span></span><br/>                | <span data-ttu-id="0c107-134">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0c107-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c107-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0c107-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c107-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c107-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c107-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c107-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c107-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c107-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c107-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c107-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c107-140">**Win32 \_ SessionResource**</span><span class="sxs-lookup"><span data-stu-id="0c107-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="0c107-141">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0c107-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
