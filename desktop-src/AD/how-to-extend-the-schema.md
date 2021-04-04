---
title: Cómo extender el esquema
description: Cuando las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee extender el esquema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Esquema AD, cómo extender
- Active Directory, usar, esquema
- Active Directory, uso, esquema, extensión del esquema, cómo extender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789520"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="e0bb2-106">Cómo extender el esquema</span><span class="sxs-lookup"><span data-stu-id="e0bb2-106">How to Extend the Schema</span></span>

<span data-ttu-id="e0bb2-107">Cuando las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee extender el esquema.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="e0bb2-108">Para obtener más información sobre cómo decidir cuándo ampliar el esquema, vea [extender el esquema](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="e0bb2-109">Una vez que haya decidido que se requiere la extensión de esquema, use el procedimiento siguiente para extender el esquema.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="e0bb2-110">Comprobar la funcionalidad de Active Directory antes de aplicar las extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="e0bb2-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="e0bb2-111">Compruebe Active Directory funcionalidad antes de actualizar el esquema para asegurarse de que la extensión de esquema se prosigue sin errores.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="e0bb2-112">Como mínimo, asegúrese de que todos los controladores de dominio del bosque estén en línea y realice la replicación de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="e0bb2-113">**Para comprobar la funcionalidad de Active Directory antes de aplicar la extensión de esquema**</span><span class="sxs-lookup"><span data-stu-id="e0bb2-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="e0bb2-114">Inicie sesión en una estación de trabajo administrativa que tenga instalada la herramienta de soporte de Windows Repadmin.exe.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="e0bb2-115">Las herramientas de soporte se encuentran en los medios de instalación del sistema operativo en la \\ carpeta Herramientas de soporte.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="e0bb2-116">Abra un símbolo del sistema y, a continuación, cambie los directorios a la carpeta en la que están instaladas las herramientas de soporte de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="e0bb2-117">En un símbolo del sistema, presione ENTER después de escribir:</span><span class="sxs-lookup"><span data-stu-id="e0bb2-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="e0bb2-118">Todos los controladores de dominio deben mostrar 0 en la columna error, y las diferencias de mayor tamaño (que indican el número de cambios realizados en la base de datos de Active Directory desde la última replicación correcta) deben ser menores o iguales que la frecuencia de replicación del vínculo a sitios que utiliza el controlador de dominio para la replicación.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="e0bb2-119">La frecuencia de replicación predeterminada es de 180 minutos.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="e0bb2-120">Para obtener más información acerca de los pasos adicionales que puede realizar para comprobar la funcionalidad de Active Directory antes de aplicar la extensión de esquema, consulte [el artículo 325379 en Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="e0bb2-121">**Para extender el esquema**</span><span class="sxs-lookup"><span data-stu-id="e0bb2-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="e0bb2-122">Determine el método de extensión.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-122">Determine the method of extension.</span></span> <span data-ttu-id="e0bb2-123">Una vez que haya diseñado cuidadosamente los cambios de esquema, el paso siguiente consiste en decidir qué método usar para extender el esquema.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="e0bb2-124">Puede utilizar alguno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="e0bb2-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="e0bb2-125">Manualmente, mediante el uso de archivos de importación.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-125">Manually, using import files.</span></span> <span data-ttu-id="e0bb2-126">Consulte la documentación sobre el [uso de la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="e0bb2-127">No use LDIFDE para importar archivos de Windows SCH \* . ldf.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="e0bb2-128">Estos archivos son necesarios para extender el esquema de Active Directory con el fin de instalar los controladores de dominio que ejecutan una versión más reciente de Windows Server que la versión que se está ejecutando en el maestro de esquema actual.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="e0bb2-129">Cuando necesite ampliar el esquema para instalar un nuevo controlador de dominio, use Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="e0bb2-130">Mediante programación, con un programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="e0bb2-131">Para obtener más información, consulte [extensión de programación](programmatic-extension.md) .</span><span class="sxs-lookup"><span data-stu-id="e0bb2-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="e0bb2-132">Habilite los cambios de esquema.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-132">Enable Schema Changes.</span></span> <span data-ttu-id="e0bb2-133">Para obtener más información, vea [requisitos previos para instalar una extensión de esquema](prerequisites-for-installing-a-schema-extension.md) y [habilitar los cambios de esquema en el maestro de esquema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="e0bb2-134">Obtenga un identificador de objeto (OID) para los nuevos atributos o clases, como se describe en [obtener un identificador de objeto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="e0bb2-135">Cree nuevos atributos y clases.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="e0bb2-136">Use especificadores de presentación para integrar nuevos atributos y clases con la interfaz de usuario, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="e0bb2-137">Actualice la caché de esquema tal y como se describe en [actualizar la caché de esquema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="e0bb2-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="e0bb2-138">Compruebe la extensión de esquema mediante LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="e0bb2-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0bb2-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0bb2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0bb2-140">Obtener un identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="e0bb2-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="e0bb2-141">Las nuevas herramientas de línea de comandos para Active Directory en Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0bb2-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="e0bb2-142">[Usar la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="e0bb2-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="e0bb2-143">[Extender el esquema de Active Directory](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e0bb2-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="e0bb2-144">Restricciones en la extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="e0bb2-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 