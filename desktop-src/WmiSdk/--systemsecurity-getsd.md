---
description: Obtiene el descriptor de seguridad para el espacio de nombres al que está conectado el usuario. Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Obtiene el método de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706471"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="a94fb-105">Método obtiene de la \_ \_ clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="a94fb-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="a94fb-106">El método que se **obtiene** obtiene el descriptor de seguridad para el espacio de nombres al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="a94fb-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="a94fb-107">Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a94fb-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="a94fb-108">Si está escribiendo un script, use el método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="a94fb-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="a94fb-109">Para obtener más información, vea [proteger los espacios de nombres WMI](securing-wmi-namespaces.md) y [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a94fb-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="a94fb-110">El usuario debe tener el permiso de **\_ control de lectura** .</span><span class="sxs-lookup"><span data-stu-id="a94fb-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="a94fb-111">De forma predeterminada, los administradores tienen ese permiso.</span><span class="sxs-lookup"><span data-stu-id="a94fb-111">By default, administrators have that permission.</span></span> <span data-ttu-id="a94fb-112">La única parte del descriptor de seguridad que se usa realmente es la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="a94fb-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="a94fb-113">DACL puede contener ACE heredadas y no heredadas.</span><span class="sxs-lookup"><span data-stu-id="a94fb-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="a94fb-114">Se permiten las ACE deny y allow.</span><span class="sxs-lookup"><span data-stu-id="a94fb-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="a94fb-115">Si está programando en C++, puede manipular el descriptor de seguridad binario mediante [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="a94fb-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="a94fb-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a94fb-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="a94fb-117">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a94fb-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94fb-118">*SD* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a94fb-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a94fb-119">Descriptor de seguridad en formato binario de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a94fb-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94fb-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a94fb-120">Return value</span></span>

<span data-ttu-id="a94fb-121">Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="a94fb-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="a94fb-122">En la lista siguiente se enumeran los valores devueltos que son de importancia para se **obtiene**.</span><span class="sxs-lookup"><span data-stu-id="a94fb-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="a94fb-123">En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a94fb-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="a94fb-124">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a94fb-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="a94fb-125">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="a94fb-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="a94fb-126">El método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a94fb-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a94fb-127">**WBEM \_ E \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="a94fb-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="a94fb-128">El autor de la llamada no tiene derechos suficientes para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="a94fb-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="a94fb-129">**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="a94fb-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="a94fb-130">Se intentó ejecutar este método en un sistema no compatible.</span><span class="sxs-lookup"><span data-stu-id="a94fb-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a94fb-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a94fb-131">Remarks</span></span>

<span data-ttu-id="a94fb-132">Para obtener más información sobre cómo modificar la seguridad de los espacios de nombres mediante programación o manualmente, consulte protección de los [espacios de nombres WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="a94fb-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a94fb-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a94fb-133">Examples</span></span>

<span data-ttu-id="a94fb-134">En el siguiente script se muestra cómo usar se **obtiene** para obtener el descriptor de seguridad actual del \\ espacio de nombres root Cimv2 y cambiarlo a la matriz de bytes que se muestra en **disjugada**.</span><span class="sxs-lookup"><span data-stu-id="a94fb-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="a94fb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a94fb-135">Requirements</span></span>



| <span data-ttu-id="a94fb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94fb-136">Requirement</span></span> | <span data-ttu-id="a94fb-137">Value</span><span class="sxs-lookup"><span data-stu-id="a94fb-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a94fb-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a94fb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a94fb-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a94fb-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a94fb-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a94fb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a94fb-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a94fb-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a94fb-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a94fb-142">Namespace</span></span><br/>                | <span data-ttu-id="a94fb-143">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="a94fb-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a94fb-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a94fb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94fb-145">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a94fb-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a94fb-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="a94fb-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a94fb-147">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="a94fb-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="a94fb-148">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a94fb-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="a94fb-149">**\_\_SystemSecurity:: establecido**</span><span class="sxs-lookup"><span data-stu-id="a94fb-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="a94fb-150">**Descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="a94fb-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="a94fb-151">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a94fb-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="a94fb-152">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="a94fb-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

