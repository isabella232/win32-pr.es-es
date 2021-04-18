---
description: El método del objeto de instalación Lee información sobre una clave del registro especificada de valor.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. método del método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653710"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="417f0-103">Installer. método del método</span><span class="sxs-lookup"><span data-stu-id="417f0-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="417f0-104">El **método del** objeto de [**instalación**](installer-object.md) Lee información sobre una clave del registro especificada de valor.</span><span class="sxs-lookup"><span data-stu-id="417f0-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="417f0-105">Si no existe la clave o el valor especificado, el método devuelve un error de 9, "Subíndice fuera del intervalo".</span><span class="sxs-lookup"><span data-stu-id="417f0-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="417f0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="417f0-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="417f0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417f0-108">*root*</span><span class="sxs-lookup"><span data-stu-id="417f0-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="417f0-109">En Windows NT 4,0, la raíz del registro es una clave raíz numérica o un nombre de equipo como una cadena.</span><span class="sxs-lookup"><span data-stu-id="417f0-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="417f0-110">Los nombres de máquina siempre son cadenas.</span><span class="sxs-lookup"><span data-stu-id="417f0-110">Machine names are always strings.</span></span> <span data-ttu-id="417f0-111">En Windows 95, Windows 98 o Windows me, la raíz del registro es solo una clave de raíz numérica.</span><span class="sxs-lookup"><span data-stu-id="417f0-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="417f0-112">Solo puede acceder a HKLM en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="417f0-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="417f0-113">Root</span><span class="sxs-lookup"><span data-stu-id="417f0-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="417f0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="417f0-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="417f0-115"><dt>**\_clase HKEY \_ raíz**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="417f0-116">0</span><span class="sxs-lookup"><span data-stu-id="417f0-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="417f0-117"><dt>**HKEY \_ Current \_ User**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="417f0-118">1</span><span class="sxs-lookup"><span data-stu-id="417f0-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="417f0-119"><dt>**HKEY \_ local \_ Machine**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="417f0-120">2</span><span class="sxs-lookup"><span data-stu-id="417f0-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="417f0-121"><dt>**\_usuarios HKEY**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="417f0-122">3</span><span class="sxs-lookup"><span data-stu-id="417f0-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="417f0-123"><dt>**\_datos de rendimiento de HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="417f0-124">4</span><span class="sxs-lookup"><span data-stu-id="417f0-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="417f0-125"><dt>**HKEY \_ \_ configuración actual**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="417f0-126">5</span><span class="sxs-lookup"><span data-stu-id="417f0-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="417f0-127"><dt>**HKEY \_ DYN \_ Data**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="417f0-128">6</span><span class="sxs-lookup"><span data-stu-id="417f0-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="417f0-129">*key*</span><span class="sxs-lookup"><span data-stu-id="417f0-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="417f0-130">Cadena que contiene la ruta de acceso de la clave completa de la raíz.</span><span class="sxs-lookup"><span data-stu-id="417f0-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="417f0-131">*value*</span><span class="sxs-lookup"><span data-stu-id="417f0-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="417f0-132">Este parámetro opcional designa el valor asociado que se va a devolver para la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="417f0-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="417f0-133">El valor es uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="417f0-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="417f0-134">Value</span><span class="sxs-lookup"><span data-stu-id="417f0-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="417f0-135">Significado</span><span class="sxs-lookup"><span data-stu-id="417f0-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="417f0-136"><dt>**Falta o está en blanco**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="417f0-137">Devuelve un valor booleano que indica si la clave existe.</span><span class="sxs-lookup"><span data-stu-id="417f0-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="417f0-138"><dt>**String@**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="417f0-139">Devuelve los datos asociados al valor con nombre, lo que produce un error si el nombre del valor no existe.</span><span class="sxs-lookup"><span data-stu-id="417f0-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="417f0-140"><dt>**Entero positivo**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="417f0-141">Devuelve el nombre del valor enumerado basado en 1, está vacío si no existe.</span><span class="sxs-lookup"><span data-stu-id="417f0-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="417f0-142">Esta opción utiliza la función [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .</span><span class="sxs-lookup"><span data-stu-id="417f0-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="417f0-143"><dt>**Entero negativo**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="417f0-144">Devuelve el nombre de la subclave enumerada basada en 1, que está vacía si no existe.</span><span class="sxs-lookup"><span data-stu-id="417f0-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="417f0-145">Esta opción utiliza la función [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .</span><span class="sxs-lookup"><span data-stu-id="417f0-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="417f0-146"><dt>**Entero cero**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="417f0-147">Devuelve el nombre de la clase de cadena para la clave designada.</span><span class="sxs-lookup"><span data-stu-id="417f0-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="417f0-148"><dt>**Cadena vacía ""**</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="417f0-149">Devuelve el valor predeterminado de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="417f0-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417f0-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417f0-150">Return value</span></span>

<span data-ttu-id="417f0-151">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="417f0-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="417f0-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417f0-152">Requirements</span></span>



| <span data-ttu-id="417f0-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="417f0-153">Requirement</span></span> | <span data-ttu-id="417f0-154">Value</span><span class="sxs-lookup"><span data-stu-id="417f0-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="417f0-155">Versión</span><span class="sxs-lookup"><span data-stu-id="417f0-155">Version</span></span><br/> | <span data-ttu-id="417f0-156">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="417f0-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="417f0-157">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="417f0-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="417f0-158">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="417f0-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="417f0-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="417f0-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="417f0-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="417f0-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="417f0-161">IID</span><span class="sxs-lookup"><span data-stu-id="417f0-161">IID</span></span><br/>     | <span data-ttu-id="417f0-162">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="417f0-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
