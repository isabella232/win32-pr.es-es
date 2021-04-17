---
description: Representa la configuración de un componente del modelo de objetos componentes (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659679"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="19756-103">\_Clase Win32 ClassicCOMClassSetting</span><span class="sxs-lookup"><span data-stu-id="19756-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="19756-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSetting de Win32** representa la configuración de un componente del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="19756-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="19756-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="19756-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="19756-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="19756-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19756-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19756-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="19756-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="19756-108">Members</span></span>

<span data-ttu-id="19756-109">La **clase \_ ClassicCOMClassSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19756-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="19756-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19756-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19756-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19756-111">Properties</span></span>

<span data-ttu-id="19756-112">La **clase \_ ClassicCOMClassSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="19756-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19756-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="19756-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-116">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-117">Identificador único global (GUID) para la aplicación COM que usa este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="19756-118">**AutoConvertToClsid**</span><span class="sxs-lookup"><span data-stu-id="19756-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-121">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} conversión automática \\ \\ \[ predeterminada \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-122">GUID de la clase COM a la que se convertirá automáticamente este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="19756-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="19756-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-126">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ autotreatas \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-127">GUID del componente COM que emulará automáticamente las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="19756-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="19756-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="19756-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-131">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="19756-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19756-132">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="19756-132">Short textual description of the current object.</span></span>

<span data-ttu-id="19756-133">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="19756-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="19756-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="19756-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-137">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-138">GUID de este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="19756-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="19756-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19756-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19756-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-142">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ control")</span><span class="sxs-lookup"><span data-stu-id="19756-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="19756-143">El componente COM es un control OLE.</span><span class="sxs-lookup"><span data-stu-id="19756-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="19756-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="19756-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-148">Ruta de acceso al archivo ejecutable y al identificador de recursos del icono predeterminado utilizado por la clase.</span><span class="sxs-lookup"><span data-stu-id="19756-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="19756-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19756-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19756-152">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="19756-152">Textual description of the current object.</span></span>

<span data-ttu-id="19756-153">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="19756-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="19756-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="19756-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-157">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-158">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en un controlador personalizado de 16 bits para el componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="19756-159">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="19756-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-163">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-164">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en un controlador personalizado de 32 bits para el componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="19756-165">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="19756-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-169">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-170">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en un archivo DLL de servidor en proceso de 16 bits para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="19756-171">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="19756-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-175">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-176">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en un archivo DLL de servidor de 32 bits para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="19756-177">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-178">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="19756-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-179">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19756-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19756-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-181">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ insertable")</span><span class="sxs-lookup"><span data-stu-id="19756-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="19756-182">El componente COM se puede insertar en aplicaciones contenedoras OLE.</span><span class="sxs-lookup"><span data-stu-id="19756-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="19756-183">**JavaClass**</span><span class="sxs-lookup"><span data-stu-id="19756-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="19756-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19756-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-186">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ JavaClass \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-187">El componente COM es un componente de Java.</span><span class="sxs-lookup"><span data-stu-id="19756-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="19756-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="19756-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-191">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-192">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en una aplicación de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="19756-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="19756-193">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="19756-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-197">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-198">Ruta de acceso completa que incluye el nombre de archivo o solo el nombre de archivo en una aplicación de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="19756-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="19756-199">El proveedor no siempre devuelve la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="19756-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="19756-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="19756-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-203">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-204">Nombre completo de la aplicación COM.</span><span class="sxs-lookup"><span data-stu-id="19756-204">Full name of the COM application.</span></span> <span data-ttu-id="19756-205">Se usa en áreas como el campo de **resultados** del cuadro de diálogo **Pegado especial de OLE** .</span><span class="sxs-lookup"><span data-stu-id="19756-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="19756-206">**Programa**</span><span class="sxs-lookup"><span data-stu-id="19756-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-209">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ predeterminado \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-210">Identificador de programación asociado al componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="19756-211">El formato de un ProgID es <versión de Vendor. <Component. <.</span><span class="sxs-lookup"><span data-stu-id="19756-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="19756-212">No se garantiza que este identificador sea único.</span><span class="sxs-lookup"><span data-stu-id="19756-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="19756-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="19756-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-216">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="19756-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19756-217">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="19756-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="19756-218">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="19756-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="19756-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="19756-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-222">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-223">Nombre corto de la aplicación COM (se usa en menús y elementos emergentes).</span><span class="sxs-lookup"><span data-stu-id="19756-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="19756-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="19756-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-227">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ ThreadingModel \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-228">Modelo de subprocesos utilizado por las clases COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="19756-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="19756-229">Si esta propiedad es **null**, no se utiliza ningún modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="19756-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="19756-230">El componente se crea en el subproceso principal del cliente y las referencias de otros subprocesos se serializan en este subproceso.</span><span class="sxs-lookup"><span data-stu-id="19756-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="19756-231">El modelo de Apartamento especifica que los componentes se pueden escribir en uno y solo un subproceso.</span><span class="sxs-lookup"><span data-stu-id="19756-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="19756-232">Los datos comunes contenidos en estos tipos de servidores de objetos deben protegerse frente a colisiones de subprocesos, ya que el servidor de objetos admite varios componentes.</span><span class="sxs-lookup"><span data-stu-id="19756-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="19756-233">Cada componente se puede especificar simultáneamente mediante distintos subprocesos.</span><span class="sxs-lookup"><span data-stu-id="19756-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="19756-234">El modelo gratuito especifica que los componentes no colocan restricciones en qué subprocesos o cuántos subprocesos pueden entrar en el objeto.</span><span class="sxs-lookup"><span data-stu-id="19756-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="19756-235">El objeto no puede contener datos específicos del subproceso y debe proteger sus datos de acceso simultáneo de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="19756-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="19756-236">Sin embargo, los subprocesos de apartamento no pueden tener acceso directamente a los componentes de subprocesos libres y se calculan las referencias a ellos a través del apartamento del cliente.</span><span class="sxs-lookup"><span data-stu-id="19756-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="19756-237">Cuando se especifican ambos, los componentes se pueden usar en los modos de subprocesamiento controlado o de subprocesos libres.</span><span class="sxs-lookup"><span data-stu-id="19756-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="19756-238">Estos componentes pueden ser especificados por varios subprocesos, proteger sus datos de colisiones de subprocesos y no contener datos específicos del subproceso.</span><span class="sxs-lookup"><span data-stu-id="19756-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="19756-239">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="19756-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="19756-240">Procesamiento</span><span class="sxs-lookup"><span data-stu-id="19756-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="19756-241">Ningún</span><span class="sxs-lookup"><span data-stu-id="19756-241">"Free"</span></span></dd> <dd><span data-ttu-id="19756-242">Ambos</span><span class="sxs-lookup"><span data-stu-id="19756-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="19756-243">**Apartamento** ("Apartamento")</span><span class="sxs-lookup"><span data-stu-id="19756-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="19756-244">**Gratis** ("gratis")</span><span class="sxs-lookup"><span data-stu-id="19756-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="19756-245">**Ambos** ("ambos")</span><span class="sxs-lookup"><span data-stu-id="19756-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19756-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="19756-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-249">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-250">Nombre del módulo y identificador de recurso para un mapa de bits pequeño (16x16) usado para el aspecto de una barra de herramientas o un botón del cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="19756-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="19756-251">Se utiliza cuando el componente COM es un control ActiveX o OLE.</span><span class="sxs-lookup"><span data-stu-id="19756-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="19756-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="19756-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-255">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ tratar \[ valores predeterminados \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-256">GUID de un componente COM que puede emular instancias de este componente.</span><span class="sxs-lookup"><span data-stu-id="19756-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="19756-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="19756-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-260">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-261">GUID de la biblioteca de tipos para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="19756-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="19756-262">**Versión**</span><span class="sxs-lookup"><span data-stu-id="19756-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-265">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ versión \[ predeterminada \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-266">Número de versión de esta clase COM.</span><span class="sxs-lookup"><span data-stu-id="19756-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="19756-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="19756-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19756-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19756-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19756-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19756-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19756-270">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ clase de software de máquina local \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="19756-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="19756-271">Identificador de programa que es coherente para todas las versiones del mismo programa.</span><span class="sxs-lookup"><span data-stu-id="19756-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19756-272">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19756-272">Remarks</span></span>

<span data-ttu-id="19756-273">La clase **Win32 \_ ClassicCOMClassSetting** se deriva de [**\_ comsetting de Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="19756-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19756-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19756-274">Requirements</span></span>



| <span data-ttu-id="19756-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="19756-275">Requirement</span></span> | <span data-ttu-id="19756-276">Value</span><span class="sxs-lookup"><span data-stu-id="19756-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19756-277">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19756-277">Minimum supported client</span></span><br/> | <span data-ttu-id="19756-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19756-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19756-279">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19756-279">Minimum supported server</span></span><br/> | <span data-ttu-id="19756-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19756-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19756-281">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19756-281">Namespace</span></span><br/>                | <span data-ttu-id="19756-282">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="19756-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19756-283">MOF</span><span class="sxs-lookup"><span data-stu-id="19756-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19756-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19756-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19756-285">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19756-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19756-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19756-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19756-287">Vea también</span><span class="sxs-lookup"><span data-stu-id="19756-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19756-288">**Establecimiento de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="19756-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="19756-289">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19756-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

