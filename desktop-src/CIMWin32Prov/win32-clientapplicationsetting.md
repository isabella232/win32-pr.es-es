---
description: La \_ clase WMI ClientApplicationSetting Association de Win32 relaciona un archivo ejecutable y una aplicación de modelo de objetos componentes (com) que contiene las opciones de configuración com del archivo ejecutable.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000733"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="7cdb3-103">\_Clase Win32 ClientApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="7cdb3-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="7cdb3-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClientApplicationSetting** Association de Win32 relaciona un archivo ejecutable y una aplicación de modelo de objetos componentes (com) que contiene las opciones de configuración com del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="7cdb3-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7cdb3-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cdb3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cdb3-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="7cdb3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7cdb3-108">Members</span></span>

<span data-ttu-id="7cdb3-109">La **clase \_ ClientApplicationSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7cdb3-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="7cdb3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cdb3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7cdb3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cdb3-111">Properties</span></span>

<span data-ttu-id="7cdb3-112">La **clase \_ ClientApplicationSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7cdb3-113">**Aplicación**</span><span class="sxs-lookup"><span data-stu-id="7cdb3-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cdb3-114">Tipo de datos: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="7cdb3-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="7cdb3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cdb3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cdb3-116">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="7cdb3-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="7cdb3-117">Referencia a la instancia de que representa la aplicación COM que contiene las opciones de configuración del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="7cdb3-118">**Cliente**</span><span class="sxs-lookup"><span data-stu-id="7cdb3-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7cdb3-119">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="7cdb3-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="7cdb3-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7cdb3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7cdb3-121">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ archivo de archivos")</span><span class="sxs-lookup"><span data-stu-id="7cdb3-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="7cdb3-122">Referencia a la instancia de que representa el archivo ejecutable que utiliza la configuración COM.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cdb3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cdb3-123">Remarks</span></span>

<span data-ttu-id="7cdb3-124">**Win32 \_ ClientApplicationSetting** no admite la enumeración.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cdb3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cdb3-125">Requirements</span></span>



| <span data-ttu-id="7cdb3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cdb3-126">Requirement</span></span> | <span data-ttu-id="7cdb3-127">Value</span><span class="sxs-lookup"><span data-stu-id="7cdb3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdb3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cdb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7cdb3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cdb3-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cdb3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cdb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7cdb3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cdb3-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cdb3-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7cdb3-132">Namespace</span></span><br/>                | <span data-ttu-id="7cdb3-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7cdb3-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7cdb3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7cdb3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cdb3-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cdb3-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cdb3-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7cdb3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cdb3-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cdb3-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cdb3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cdb3-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="7cdb3-139">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cdb3-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

