---
title: Deshabilitar clases y atributos existentes
description: Las adiciones de esquema son permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773249"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="bab9c-103">Deshabilitar clases y atributos existentes</span><span class="sxs-lookup"><span data-stu-id="bab9c-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="bab9c-104">Las adiciones de esquema son permanentes.</span><span class="sxs-lookup"><span data-stu-id="bab9c-104">Schema additions are permanent.</span></span> <span data-ttu-id="bab9c-105">No se pueden eliminar los objetos **attributeSchema** y **ClassSchema** .</span><span class="sxs-lookup"><span data-stu-id="bab9c-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="bab9c-106">En un sistema distribuido, es difícil garantizar que no haya instancias de una clase o un atributo determinados.</span><span class="sxs-lookup"><span data-stu-id="bab9c-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="bab9c-107">La eliminación de la definición de una clase o atributo daña las instancias existentes de esa clase o atributo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="bab9c-108">Puede deshabilitar una clase o un atributo existente marcándolos como "inactivo".</span><span class="sxs-lookup"><span data-stu-id="bab9c-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="bab9c-109">Esto no afecta a las instancias existentes de la clase o atributo, así que impide la creación de nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="bab9c-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="bab9c-110">Al deshabilitar las clases y atributos de esquema se aplican las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="bab9c-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="bab9c-111">No se puede deshabilitar una clase o atributo de categoría 1.</span><span class="sxs-lookup"><span data-stu-id="bab9c-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="bab9c-112">No se puede deshabilitar un atributo que sea miembro de una clase que no esté también deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="bab9c-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="bab9c-113">Esto se debe a que es posible que se requiera un atributo para la clase (no deshabilitada) y al deshabilitar el atributo se evita que se creen nuevas instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="bab9c-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="bab9c-114">Para deshabilitar un atributo, establezca el atributo **isDefunct** de su objeto **attributeSchema** en **true**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="bab9c-115">Cuando un atributo está deshabilitado, no se pueden crear nuevas instancias del atributo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="bab9c-116">Para volver a habilitar el atributo, establezca el atributo **isDefunct** en **false**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="bab9c-117">Para deshabilitar una clase, establezca el atributo **isDefunct** de su objeto **ClassSchema** en **true**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="bab9c-118">Cuando se deshabilita una clase, no se pueden crear nuevas instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="bab9c-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="bab9c-119">Para volver a habilitar la clase, establezca el atributo **isDefunct** en **false**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="bab9c-120">La configuración de objetos de esquema como inactivos puede ser útil en entornos de producción.</span><span class="sxs-lookup"><span data-stu-id="bab9c-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="bab9c-121">Cuando ya no se necesite una versión de prueba de una extensión de esquema, márquela como inactiva.</span><span class="sxs-lookup"><span data-stu-id="bab9c-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="bab9c-122">Puede restaurarlo quitando el atributo **isDefunct** o estableciendo el valor del atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="bab9c-123">Esto también protege contra una eliminación imprevista de un objeto de esquema estableciéndolo en inactivo porque la operación se puede invertir fácilmente.</span><span class="sxs-lookup"><span data-stu-id="bab9c-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="bab9c-124">Tenga en cuenta que el servidor de Active Directory no limpia las instancias existentes de un atributo o clase cuando se hace que un objeto de esquema esté inactivo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="bab9c-125">Si quita la propiedad **isDefunct** , todas las instancias volverán a ser objetos normales válidos.</span><span class="sxs-lookup"><span data-stu-id="bab9c-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="bab9c-126">La lista siguiente incluye otras consecuencias de marcar un objeto **attributeSchema** o **ClassSchema** como inactivo:</span><span class="sxs-lookup"><span data-stu-id="bab9c-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="bab9c-127">Se produce un error al agregar o modificar una instancia.</span><span class="sxs-lookup"><span data-stu-id="bab9c-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="bab9c-128">Los códigos de error se comportan como si nunca existiera una clase inactiva.</span><span class="sxs-lookup"><span data-stu-id="bab9c-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="bab9c-129">Buscar y eliminar se comportan como si no se hubieran creado objetos de esquema inactivos.</span><span class="sxs-lookup"><span data-stu-id="bab9c-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="bab9c-130">Solo se permite la eliminación de un atributo completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="bab9c-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="bab9c-131">La lista siguiente incluye opciones adicionales en un entorno de producción para reducir el impacto de las extensiones de esquema inactivas:</span><span class="sxs-lookup"><span data-stu-id="bab9c-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="bab9c-132">Quite todos los valores de atributo **mayHave** de una clase inactiva.</span><span class="sxs-lookup"><span data-stu-id="bab9c-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="bab9c-133">Reduzca el tamaño de todos los valores de atributo **mustHave** de una clase inactiva.</span><span class="sxs-lookup"><span data-stu-id="bab9c-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="bab9c-134">Quitar un atributo inactivo del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="bab9c-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="bab9c-135">Quitar un atributo inactivo de cualquier índice.</span><span class="sxs-lookup"><span data-stu-id="bab9c-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="bab9c-136">Otras opciones para quitar los cambios de esquema no deseados en un entorno de producción son para que los desarrolladores usen un controlador de dominio privado para las pruebas.</span><span class="sxs-lookup"><span data-stu-id="bab9c-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="bab9c-137">En este caso, puede:</span><span class="sxs-lookup"><span data-stu-id="bab9c-137">In this case, you can:</span></span>

-   <span data-ttu-id="bab9c-138">"Restablezca" el servidor de Active Directory mediante Dcpromo.exe para disminuir de nivel el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="bab9c-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="bab9c-139">Una vez finalizada la degradación, vuelva a usar Dcpromo.exe para promover el servidor a un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="bab9c-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="bab9c-140">A continuación, el desarrollador puede usar scripts LDIF para volver a cargar las clases, los atributos y las instancias de objeto necesarios.</span><span class="sxs-lookup"><span data-stu-id="bab9c-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="bab9c-141">Use Ntbackup.exe para realizar una copia de seguridad del estado del sistema en una partición de disco disponible.</span><span class="sxs-lookup"><span data-stu-id="bab9c-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="bab9c-142">Reinicie el modo seguro o de restauración del servicio de directorio para restaurar.</span><span class="sxs-lookup"><span data-stu-id="bab9c-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="bab9c-143">En el caso de los sistemas operativos Windows Server 2003, cuando se establece una clase o un atributo en inactivo, se pueden volver a usar inmediatamente los valores **LDAPDisplayName**, **schemaIdGuid**, **OID** y **mapiID** del elemento de esquema inactivo al crear una nueva clase o atributo para reemplazarlo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="bab9c-144">La versión inactiva de la clase o atributo se mantiene en el contenedor de esquema, pero está oculta en el complemento MMC.</span><span class="sxs-lookup"><span data-stu-id="bab9c-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="bab9c-145">Para reactivar el elemento de esquema anterior, establezca **isDefunct** en **false**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="bab9c-146">En el ejemplo de código LDIF siguiente se muestra cómo modificar el atributo **isDefunct** y cambiar el RDN para que no se confunda con la nueva clase que se crea para reemplazarlo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="bab9c-147">Use el siguiente comando para ejecutar el ejemplo de código LDIF en un bosque de un equipo que se ejecuta en sistemas operativos Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bab9c-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="bab9c-148">**LDIFDE/i/f RDN. ldf/c "DC = X" "DC = miDominio, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="bab9c-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="bab9c-149">(Donde "DC = X" es una constante)</span><span class="sxs-lookup"><span data-stu-id="bab9c-149">(Where "DC=X" is a constant)</span></span>

 

 




