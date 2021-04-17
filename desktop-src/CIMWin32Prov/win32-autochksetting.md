---
description: La \_ clase WMI AutochkSetting de Win32 representa la configuración de la operación de comprobación de un disco.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659713"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="6b2fc-103">\_Clase Win32 AutochkSetting</span><span class="sxs-lookup"><span data-stu-id="6b2fc-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="6b2fc-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ AutochkSetting de Win32** representa la configuración de la operación de comprobación de un disco.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="6b2fc-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6b2fc-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2fc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b2fc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="6b2fc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b2fc-108">Members</span></span>

<span data-ttu-id="6b2fc-109">La **clase \_ AutochkSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b2fc-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6b2fc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b2fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b2fc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b2fc-111">Properties</span></span>

<span data-ttu-id="6b2fc-112">La **clase \_ AutochkSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b2fc-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2fc-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b2fc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6b2fc-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6b2fc-117">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-117">Short textual description of the current object.</span></span>

<span data-ttu-id="6b2fc-118">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6b2fc-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2fc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2fc-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b2fc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b2fc-122">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-122">Textual description of the current object.</span></span>

<span data-ttu-id="6b2fc-123">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6b2fc-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b2fc-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2fc-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b2fc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-127">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b2fc-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6b2fc-128">IDENTIFICADOR que se usa como parte de una clave para el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="6b2fc-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b2fc-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b2fc-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6b2fc-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \| AutoChkTimeOut"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="6b2fc-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6b2fc-133">Retraso de entrada del usuario para la comprobación.</span><span class="sxs-lookup"><span data-stu-id="6b2fc-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b2fc-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b2fc-134">Remarks</span></span>

<span data-ttu-id="6b2fc-135">La **clase \_ AutochkSetting de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6b2fc-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2fc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b2fc-136">Requirements</span></span>



| <span data-ttu-id="6b2fc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b2fc-137">Requirement</span></span> | <span data-ttu-id="6b2fc-138">Value</span><span class="sxs-lookup"><span data-stu-id="6b2fc-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2fc-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b2fc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2fc-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b2fc-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b2fc-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b2fc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2fc-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b2fc-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b2fc-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b2fc-143">Namespace</span></span><br/>                | <span data-ttu-id="6b2fc-144">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6b2fc-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b2fc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="6b2fc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b2fc-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b2fc-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b2fc-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b2fc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b2fc-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b2fc-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2fc-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b2fc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2fc-150">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="6b2fc-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="6b2fc-151">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="6b2fc-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

