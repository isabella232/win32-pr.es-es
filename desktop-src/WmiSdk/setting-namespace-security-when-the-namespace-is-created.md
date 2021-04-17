---
title: Establecer la seguridad en la creación de espacios de nombres
description: El archivo Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de seguridad para el espacio de nombres incluyendo el calificador NamespaceSecuritySDDL con el descriptor de seguridad en el formato de lenguaje de definición de descriptores de seguridad (SDDL).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546875"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="3f261-103">Establecer la seguridad en la creación de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="3f261-103">Setting security on namespace creation</span></span>

<span data-ttu-id="3f261-104">El archivo Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de [*seguridad*](/windows/desktop/SecGloss/s-gly) para el espacio de nombres incluyendo el calificador **NamespaceSecuritySDDL** con el descriptor de seguridad en el formato de [lenguaje de definición de descriptores de seguridad (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="3f261-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="3f261-105">Puede usar **NamespaceSecuritySDDL** para proteger cualquier espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="3f261-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="3f261-106">También puede usar este calificador en un archivo MOF simple para modificar el descriptor de seguridad de un espacio de nombres existente.</span><span class="sxs-lookup"><span data-stu-id="3f261-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="3f261-107">WMI procesa la cadena SDDL para establecer la seguridad del espacio de nombres, pero no se almacena como una cadena.</span><span class="sxs-lookup"><span data-stu-id="3f261-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="3f261-108">Si no se especifica ningún descriptor de seguridad, se usa la seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f261-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="3f261-109">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="3f261-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="3f261-110">El siguiente procedimiento establece el descriptor de seguridad para el espacio de nombres de la *raíz \\* myNameSpace.</span><span class="sxs-lookup"><span data-stu-id="3f261-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="3f261-111">La cadena SDDL establece el propietario y el grupo en usuarios autenticados y especifica una [*lista de control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) que heredan los espacios de nombres secundarios.</span><span class="sxs-lookup"><span data-stu-id="3f261-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="3f261-112">La DACL permite al usuario leer datos, ejecutar métodos, escribir datos en clases de proveedor y usar el acceso remoto: **WBEM \_ enable**, **WBEM \_ Method \_ Execute**, **WBEM \_ Write \_ Provider**, WBEM **\_ Remote \_ Access**.</span><span class="sxs-lookup"><span data-stu-id="3f261-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="3f261-113">Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="3f261-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="3f261-114">**Para establecer una DACL de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="3f261-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="3f261-115">Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que define el espacio de nombres para agregar el calificador **NamespaceSecuritySDDL** con la cadena SDDL.</span><span class="sxs-lookup"><span data-stu-id="3f261-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="3f261-116">En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es la raíz \\ myNameSpace y el archivo se denomina myNameSpace \_ Security. mof.</span><span class="sxs-lookup"><span data-stu-id="3f261-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="3f261-117">Tenga en cuenta que la cadena SDDL distingue entre mayúsculas y minúsculas: las letras deben escribirse en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="3f261-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="3f261-118">En el ejemplo de código siguiente se muestran las letras "o" y "g" en la cadena SDDL en minúsculas, lo que hará que Mofcomp.exe devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="3f261-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="3f261-119">Ejecute [**Mofcomp.exe**](mofcomp.md) para compilar el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="3f261-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="3f261-120">**c: \\ MOFCOMP myNameSpace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="3f261-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="3f261-121">En C++, utilice los métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="3f261-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="3f261-122">Si se produce un error al intentar establecer la DACL del espacio de nombres, tenga en cuenta los siguientes mensajes de error:</span><span class="sxs-lookup"><span data-stu-id="3f261-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="3f261-123">Error</span><span class="sxs-lookup"><span data-stu-id="3f261-123">Error</span></span>                           | <span data-ttu-id="3f261-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f261-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3f261-125">**\_ \_ parámetro no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="3f261-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="3f261-126">No hay ninguna DACL heredada.</span><span class="sxs-lookup"><span data-stu-id="3f261-126">There is no inherited DACL.</span></span> <span data-ttu-id="3f261-127">Como alternativa, el autor de la llamada ha infringido la DACL o el SD en el espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="3f261-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="3f261-128">**WBEM \_ E \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="3f261-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="3f261-129">El autor de la llamada no tiene permiso para actualizar el SDDL en MOF.</span><span class="sxs-lookup"><span data-stu-id="3f261-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="3f261-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f261-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f261-131">Configuración de descriptores de seguridad de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="3f261-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="3f261-132">**Constantes de derechos de acceso de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="3f261-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="3f261-133">**Constantes de marca ACE de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="3f261-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="3f261-134">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="3f261-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
