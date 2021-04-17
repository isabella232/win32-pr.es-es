---
description: Establece el descriptor de seguridad para el espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Método establecido de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687694"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="283d5-105">Método establecido de la \_ \_ clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="283d5-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="283d5-106">El método **sets** establece el descriptor de seguridad para el espacio de nombres al que está conectado un usuario.</span><span class="sxs-lookup"><span data-stu-id="283d5-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="283d5-107">Este método requiere un descriptor de seguridad en formato binario de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="283d5-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="283d5-108">Si está escribiendo un script, use el método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="283d5-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="283d5-109">Para obtener más información, vea [proteger los espacios de nombres WMI](securing-wmi-namespaces.md) y [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="283d5-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="283d5-110">Si está programando en C++, puede manipular el descriptor de seguridad binario mediante [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="283d5-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="283d5-111">Un usuario debe tener el permiso **escribir \_ DAC** y, de forma predeterminada, un administrador tiene ese permiso.</span><span class="sxs-lookup"><span data-stu-id="283d5-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="283d5-112">La única parte del descriptor de seguridad que se usa es la entrada de control de acceso (ACE) no heredada en la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="283d5-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="283d5-113">Al establecer la marca de **\_ herencia de contenedor** en las ACE, el descriptor de seguridad afecta a los espacios de nombres secundarios.</span><span class="sxs-lookup"><span data-stu-id="283d5-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="283d5-114">Se permiten las ACE de permitir y denegar.</span><span class="sxs-lookup"><span data-stu-id="283d5-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="283d5-115">Dado que las ACE deny y Allow se permiten en una DACL, el orden de las ACE es importante.</span><span class="sxs-lookup"><span data-stu-id="283d5-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="283d5-116">Para obtener más información, vea [ordenación de ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="283d5-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="283d5-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="283d5-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="283d5-118">Parámetros</span><span class="sxs-lookup"><span data-stu-id="283d5-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="283d5-119">*SD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="283d5-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283d5-120">Matriz de bytes que constituye el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="283d5-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="283d5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="283d5-121">Return value</span></span>

<span data-ttu-id="283d5-122">Devuelve un **valor HRESULT** que indica el estado de una llamada al método.</span><span class="sxs-lookup"><span data-stu-id="283d5-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="283d5-123">En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="283d5-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="283d5-124">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="283d5-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="283d5-125">En la lista siguiente se enumeran los valores devueltos que son significativos para los **conjuntos**.</span><span class="sxs-lookup"><span data-stu-id="283d5-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="283d5-126">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="283d5-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="283d5-127">El método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="283d5-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="283d5-128">**WBEM \_ E \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="283d5-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="283d5-129">El autor de la llamada no tiene derechos suficientes para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="283d5-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="283d5-130">**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="283d5-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="283d5-131">Se intentó ejecutar este método en el sistema operativo que no lo admite.</span><span class="sxs-lookup"><span data-stu-id="283d5-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="283d5-132">**\_ \_ objeto no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="283d5-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="283d5-133">SD no pasa las pruebas de validez básicas.</span><span class="sxs-lookup"><span data-stu-id="283d5-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="283d5-134">**\_ \_ parámetro no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="283d5-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="283d5-135">SD no es válido debido a uno de los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="283d5-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="283d5-136">Falta DACL.</span><span class="sxs-lookup"><span data-stu-id="283d5-136">DACL is missing.</span></span>
-   <span data-ttu-id="283d5-137">DACL no válida.</span><span class="sxs-lookup"><span data-stu-id="283d5-137">DACL is not valid.</span></span>
-   <span data-ttu-id="283d5-138">ACE tiene establecida la marca de representador de **\_ \_ escritura completa \_ de WBEM** y no se ha establecido la marca de proveedor de escritura de WBEM o de **\_ \_ proveedor** de escritura WBEM **\_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="283d5-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="283d5-139">ACE tiene la **marca \_ \_ ACE de solo heredar** establecida sin la marca de la **\_ \_ ACE de herencia de contenedor** .</span><span class="sxs-lookup"><span data-stu-id="283d5-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="283d5-140">ACE tiene un conjunto de bits de acceso desconocido.</span><span class="sxs-lookup"><span data-stu-id="283d5-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="283d5-141">ACE tiene un conjunto de marcas que no está en la tabla.</span><span class="sxs-lookup"><span data-stu-id="283d5-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="283d5-142">La ACE tiene un tipo que no está en la tabla.</span><span class="sxs-lookup"><span data-stu-id="283d5-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="283d5-143">Faltan el propietario y el grupo en SD.</span><span class="sxs-lookup"><span data-stu-id="283d5-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="283d5-144">Para obtener más información sobre las marcas de entrada de control de acceso (ACE), consulte [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="283d5-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="283d5-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="283d5-145">Remarks</span></span>

<span data-ttu-id="283d5-146">Para obtener más información sobre cómo modificar la seguridad de los espacios de nombres mediante programación o manualmente, consulte protección de los [espacios de nombres WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="283d5-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="283d5-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="283d5-147">Examples</span></span>

<span data-ttu-id="283d5-148">En el script siguiente se muestra cómo **usar** seted para establecer el descriptor de seguridad del espacio de nombres para el espacio de nombres raíz y cambiarlo a la matriz de bytes que se muestra en *strSD*.</span><span class="sxs-lookup"><span data-stu-id="283d5-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="283d5-149">En el siguiente ejemplo de código de C# se usa System. Security. AccessControl. RawSecurityDescriptor para enumerar, insertar y quitar nuevos objetos CommonAce en RawSecurityDescriptor. DiscretionaryAcl y, a continuación, volver a convertirlos en una matriz de bytes para guardarlos a través de establecido.</span><span class="sxs-lookup"><span data-stu-id="283d5-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="283d5-150">Un SecurityIdentifier se puede recuperar mediante NTAccount y translate.</span><span class="sxs-lookup"><span data-stu-id="283d5-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="283d5-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="283d5-151">Requirements</span></span>



| <span data-ttu-id="283d5-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="283d5-152">Requirement</span></span> | <span data-ttu-id="283d5-153">Value</span><span class="sxs-lookup"><span data-stu-id="283d5-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="283d5-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="283d5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="283d5-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="283d5-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="283d5-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="283d5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="283d5-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="283d5-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="283d5-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="283d5-158">Namespace</span></span><br/>                | <span data-ttu-id="283d5-159">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="283d5-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="283d5-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="283d5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283d5-161">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="283d5-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="283d5-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="283d5-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="283d5-163">**\_\_SystemSecurity:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="283d5-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="283d5-164">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="283d5-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="283d5-165">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="283d5-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="283d5-166">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="283d5-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="283d5-167">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="283d5-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

