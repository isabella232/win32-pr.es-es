---
title: Scripts LDIF
description: El formato de intercambio de datos LDAP (LDIF) es un estándar de Internet Engineering Task Force (IETF) que define cómo importar y exportar los datos de directorio entre los servidores de directorio que usan proveedores de servicios LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory de scripts LDIF
- Scripts LDIF Active Directory, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994971"
---
# <a name="ldif-scripts"></a><span data-ttu-id="88fc9-105">Scripts LDIF</span><span class="sxs-lookup"><span data-stu-id="88fc9-105">LDIF Scripts</span></span>

<span data-ttu-id="88fc9-106">El formato de intercambio de datos LDAP (LDIF) es un estándar de Internet Engineering Task Force (IETF) que define cómo importar y exportar los datos de directorio entre los servidores de directorio que usan proveedores de servicios LDAP.</span><span class="sxs-lookup"><span data-stu-id="88fc9-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="88fc9-107">Windows 2000 y Windows Server 2003 incluyen una utilidad de línea de comandos, LDIFDE, que se puede usar para importar objetos de directorio en Active Directory Domain Services mediante archivos LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="88fc9-108">LDIFDE permite establecer un filtro en una cadena específica para buscar y enumerar objetos de directorio en Active Directory Domain Services como archivos LDIF que los administradores de esquema pueden leer fácilmente.</span><span class="sxs-lookup"><span data-stu-id="88fc9-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="88fc9-109">Al importar un archivo Unicode, LDIFDE importa el archivo como Unicode si contiene el identificador Unicode al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="88fc9-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="88fc9-110">Si desea importar un archivo como Unicode cuando no contiene el identificador Unicode al principio del archivo, puede usar el modificador-u para obligar a que se importe como Unicode de.</span><span class="sxs-lookup"><span data-stu-id="88fc9-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="88fc9-111">El modo predeterminado para exportar archivos es ANSI.</span><span class="sxs-lookup"><span data-stu-id="88fc9-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="88fc9-112">Si hay entradas Unicode, se convertirán al formato 64 de base.</span><span class="sxs-lookup"><span data-stu-id="88fc9-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="88fc9-113">Para exportar un archivo al formato Unicode, use el modificador-u.</span><span class="sxs-lookup"><span data-stu-id="88fc9-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="88fc9-114">Un archivo LDIF debe aplicar cambios de esquema cuando hay dependencias entre los atributos que se agregan.</span><span class="sxs-lookup"><span data-stu-id="88fc9-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="88fc9-115">Por ejemplo, los atributos de vínculo hacia delante deben agregarse antes del atributo de vínculo de retroceso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="88fc9-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="88fc9-116">También debe actualizar la caché de esquema antes de agregar clases que dependan de atributos o clases agregadas anteriormente en el script LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="88fc9-117">Para obtener más información, vea el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="88fc9-117">For more information, see the following code example.</span></span>

<span data-ttu-id="88fc9-118">Tenga en cuenta que para los valores binarios, debe codificar los valores como Base64.</span><span class="sxs-lookup"><span data-stu-id="88fc9-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="88fc9-119">La codificación Base64 se define en IETF RFC 2045, sección 6,8.</span><span class="sxs-lookup"><span data-stu-id="88fc9-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="88fc9-120">Para obtener más información sobre el formato de los archivos LDIF, vea [el formato de intercambio de datos LDAP (LDIF): Especificación técnica](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) en el sitio web de Internet Engineering Task Force.</span><span class="sxs-lookup"><span data-stu-id="88fc9-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="88fc9-121">Changetypes LDIF específico de NTDS</span><span class="sxs-lookup"><span data-stu-id="88fc9-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="88fc9-122">Es mejor usar ntdsSchema \* changetypes en lugar de llamar a LDIFDE-k.</span><span class="sxs-lookup"><span data-stu-id="88fc9-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="88fc9-123">La opción-k de LDIFDE omite un conjunto mayor de errores LDAP.</span><span class="sxs-lookup"><span data-stu-id="88fc9-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="88fc9-124">La lista completa de errores omitidos es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="88fc9-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="88fc9-125">El objeto ya es miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="88fc9-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="88fc9-126">Una infracción de clase de objeto (lo que significa que la clase de objeto especificada no existe) si el objeto que se importa no tiene otros atributos.</span><span class="sxs-lookup"><span data-stu-id="88fc9-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="88fc9-127">el objeto ya existe (**LDAP \_ ya \_ existe**)</span><span class="sxs-lookup"><span data-stu-id="88fc9-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="88fc9-128">infracción de restricción (**\_ \_ infracción de restricción LDAP**)</span><span class="sxs-lookup"><span data-stu-id="88fc9-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="88fc9-129">el atributo o valor ya existe **( \_ existe el atributo \_ o el \_ valor \_ LDAP**)</span><span class="sxs-lookup"><span data-stu-id="88fc9-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="88fc9-130">no se trata de un objeto de este tipo (**LDAP \_ no es \_ tal \_**)</span><span class="sxs-lookup"><span data-stu-id="88fc9-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="88fc9-131">Los siguientes changetypes están diseñados específicamente para las operaciones de actualización del esquema.</span><span class="sxs-lookup"><span data-stu-id="88fc9-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="88fc9-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="88fc9-132">Changetype</span></span>                      | <span data-ttu-id="88fc9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="88fc9-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fc9-134">**ntdsSchemaAdd**</span><span class="sxs-lookup"><span data-stu-id="88fc9-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="88fc9-135">**ntdsSchemaAdd** se corresponde con **Agregar** en un archivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="88fc9-136">La única diferencia es que **ntdsSchemaAdd** haría que LDIFDE omitiera una operación de **adición** si el objeto ya existe en el esquema.</span><span class="sxs-lookup"><span data-stu-id="88fc9-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="88fc9-137">(**LDAP \_ ya \_ existe** se omite).</span><span class="sxs-lookup"><span data-stu-id="88fc9-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="88fc9-138">**ntdsSchemaModify**</span><span class="sxs-lookup"><span data-stu-id="88fc9-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="88fc9-139">**ntdsSchemaModify** se corresponde con la **modificación** en un archivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="88fc9-140">La única diferencia es que **ntdsSchemaModify** haría que LDIFDE omitira una operación de **modificación** si el objeto no se encuentra en el esquema.</span><span class="sxs-lookup"><span data-stu-id="88fc9-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="88fc9-141">(**LDAP \_ no se omite \_ este \_ objeto** ).</span><span class="sxs-lookup"><span data-stu-id="88fc9-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="88fc9-142">**ntdsSchemaDelete**</span><span class="sxs-lookup"><span data-stu-id="88fc9-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="88fc9-143">**ntdsSchemaDelete** corresponde a **Delete** en un archivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="88fc9-144">La única diferencia es que **ntdsSchemaDelete** haría que LDIFDE omitira una operación de **eliminación** si el objeto no se encuentra en el esquema.</span><span class="sxs-lookup"><span data-stu-id="88fc9-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="88fc9-145">(**LDAP \_ no se omite \_ este \_ objeto** ).</span><span class="sxs-lookup"><span data-stu-id="88fc9-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="88fc9-146">**ntdsSchemaModRdn**</span><span class="sxs-lookup"><span data-stu-id="88fc9-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="88fc9-147">**ntdsSchemaModRdn** corresponde a **modrdn** en un archivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="88fc9-148">La única diferencia es que **ntdsSchemaModRdn** haría que LDIFDE omitira una operación de nombre distintivo de modificación relativa si el objeto no se encuentra en el esquema.</span><span class="sxs-lookup"><span data-stu-id="88fc9-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="88fc9-149">(**LDAP \_ no se omite \_ este \_ objeto** ).</span><span class="sxs-lookup"><span data-stu-id="88fc9-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="88fc9-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88fc9-150">Example</span></span>

<span data-ttu-id="88fc9-151">El siguiente ejemplo de código incluye:</span><span class="sxs-lookup"><span data-stu-id="88fc9-151">The following code example includes:</span></span>

-   <span data-ttu-id="88fc9-152">Myschemaext. ldf es un script LDIF que contiene nuevos atributos y clases.</span><span class="sxs-lookup"><span data-stu-id="88fc9-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="88fc9-153">Tenga en cuenta que este archivo es una versión modificada del archivo generado a partir de Lgetattcls.vbs.</span><span class="sxs-lookup"><span data-stu-id="88fc9-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="88fc9-154">Tenga en cuenta también que el atributo **My-test-Attribute-DN-FL** se ha desplazado por delante de **My-test-Attribute-DN-BL** porque el vínculo de retroceso (**My-test-Attribute-DN-BL**) depende del vínculo hacia delante (**My-test-Attribute-DN-FL**).</span><span class="sxs-lookup"><span data-stu-id="88fc9-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="88fc9-155">Además, el atributo operativo **schemaUpdateNow** se establece en dos lugares para desencadenar actualizaciones de la caché de esquema de modo que los atributos y las clases dependientes estén disponibles para agregar las dos clases en el script.</span><span class="sxs-lookup"><span data-stu-id="88fc9-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="88fc9-156">Vea el tema [obtener un identificador de vínculo](obtaining-a-link-id.md) para obtener información sobre el origen del identificador en las instrucciones LinkId:.</span><span class="sxs-lookup"><span data-stu-id="88fc9-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="88fc9-157">Lgetattcls.vbs es un archivo de VBScript que genera el script LDIF que se usa como punto de partida para Myschemaext. ldf.</span><span class="sxs-lookup"><span data-stu-id="88fc9-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="88fc9-158">Tenga en cuenta que la ruta de acceso del esquema actual se ha reemplazado por CN = Schema, CN = Configuration, DC = myorg, DC = com.</span><span class="sxs-lookup"><span data-stu-id="88fc9-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="88fc9-159">Puede reemplazar DC = myorg, DC = com para reflejar el nombre distintivo (DN) que se va a publicar en el script LDIF. Asegúrese de que LSETATTCLS.VBS refleje el cambio en su **sFromDN** para que el DN correcto se reemplace cuando se aplique el script LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="88fc9-160">Tenga en cuenta también que el script usa un prefijo para buscar las clases y los atributos que también debe definir y usar un prefijo para todas las clases y atributos.</span><span class="sxs-lookup"><span data-stu-id="88fc9-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="88fc9-161">Para obtener más información, vea [naming Attributes and classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="88fc9-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="88fc9-162">Además, el script genera solo los atributos necesarios para los objetos **attributeSchema** y **ClassSchema** en el archivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="88fc9-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="88fc9-163">Lsetattcls.vbs es un archivo de VBScript que usa el script Myschemaext. ldf para agregar los nuevos atributos y clases en el script.</span><span class="sxs-lookup"><span data-stu-id="88fc9-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="88fc9-164">Asegúrese de que se puede escribir en el maestro de esquema antes de ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="88fc9-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="88fc9-165">MYSCHEMAEXT. LDF</span><span class="sxs-lookup"><span data-stu-id="88fc9-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="88fc9-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="88fc9-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="88fc9-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="88fc9-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





