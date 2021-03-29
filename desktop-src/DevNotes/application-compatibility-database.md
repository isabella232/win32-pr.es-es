---
description: La infraestructura de compatibilidad utiliza una base de datos para identificar los problemas de compatibilidad de aplicaciones y sus soluciones.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Base de datos de compatibilidad de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807124"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="76e92-103">Base de datos de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="76e92-103">Application Compatibility Database</span></span>

<span data-ttu-id="76e92-104">La infraestructura de compatibilidad utiliza una base de datos para identificar los problemas de compatibilidad de aplicaciones y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="76e92-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="76e92-105">Esta base de datos es un archivo binario indexado con una extensión. sdb.</span><span class="sxs-lookup"><span data-stu-id="76e92-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="76e92-106">La infraestructura de compatibilidad proporciona una interfaz de programación para tener acceso a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="76e92-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="76e92-107">Los problemas de compatibilidad se pueden resolver de forma programa por aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="76e92-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="76e92-108">Cada aplicación especificada en la base de datos contiene uno o más componentes que necesitan una solución.</span><span class="sxs-lookup"><span data-stu-id="76e92-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="76e92-109">Los componentes son archivos ejecutables que se describen normalmente con sus atributos de archivo (por ejemplo, checksum).</span><span class="sxs-lookup"><span data-stu-id="76e92-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="76e92-110">El proceso de búsqueda en la base de datos y la determinación de las soluciones para cada aplicación se denomina *coincidencia*.</span><span class="sxs-lookup"><span data-stu-id="76e92-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="76e92-111">Los atributos de archivo y la presencia de archivos asociados en la carpeta o subcarpeta que contiene el archivo. exe se pueden usar para crear una coincidencia única.</span><span class="sxs-lookup"><span data-stu-id="76e92-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="76e92-112">Los archivos asociados se denominan *archivos coincidentes*.</span><span class="sxs-lookup"><span data-stu-id="76e92-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="76e92-113">Una *etiqueta* es un identificador único para las entradas y atributos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="76e92-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="76e92-114">El *tipo de etiqueta* indica el formato de los datos asociados a la [**etiqueta**](tag.md).</span><span class="sxs-lookup"><span data-stu-id="76e92-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="76e92-115">Por ejemplo, **el \_ nombre** de etiqueta es de tipo **tag \_ Type \_ STRINGREF**; los datos de **\_ nombre de etiqueta** son una cadena de nombre.</span><span class="sxs-lookup"><span data-stu-id="76e92-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="76e92-116">Un *TAGID* es un puntero a una entrada en una base de datos determinada.</span><span class="sxs-lookup"><span data-stu-id="76e92-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="76e92-117">Un *TAGREF* es un puntero a una entrada que se puede usar en varias bases de datos.</span><span class="sxs-lookup"><span data-stu-id="76e92-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="76e92-118">*Los atributos de archivo* son metadatos asociados a un archivo en disco.</span><span class="sxs-lookup"><span data-stu-id="76e92-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="76e92-119">Estos atributos incluyen el nombre de archivo, el tamaño del archivo, la suma de comprobación, la versión y la fecha.</span><span class="sxs-lookup"><span data-stu-id="76e92-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="76e92-120">Estos atributos se usan para determinar si un archivo cargado por el sistema coincide con una entrada de base de datos.</span><span class="sxs-lookup"><span data-stu-id="76e92-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="76e92-121">Por lo tanto, estos atributos de archivo también se denominan *atributos coincidentes*.</span><span class="sxs-lookup"><span data-stu-id="76e92-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="76e92-122">Soluciones</span><span class="sxs-lookup"><span data-stu-id="76e92-122">Solutions</span></span>

<span data-ttu-id="76e92-123">Las soluciones más comunes aplicadas a los componentes de una aplicación son apphelp y AppFix.</span><span class="sxs-lookup"><span data-stu-id="76e92-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="76e92-124">Con apphelp, se muestra una notificación de mensajes localizados personalizada, normalmente cuando se instala o se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76e92-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="76e92-125">Contiene texto breve que explica el problema de compatibilidad y proporciona la opción de seguir ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76e92-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="76e92-126">Sin embargo, se permite que se ejecuten drásticamente algunas aplicaciones. Apphelp no ofrece al usuario la opción de seguir ejecutando estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="76e92-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="76e92-127">Con AppFix, se instalan enlaces para las API a las que llaman los componentes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76e92-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="76e92-128">Estos enlaces apuntan a funciones de código auxiliar a las que se puede llamar en lugar de a las funciones del sistema (también conocidas como *SHIMMING*).</span><span class="sxs-lookup"><span data-stu-id="76e92-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="76e92-129">Las funciones de código auxiliar realizan las operaciones necesarias para permitir que la aplicación se ejecute en la versión instalada de Windows.</span><span class="sxs-lookup"><span data-stu-id="76e92-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="76e92-130">Cada función de código auxiliar puede llamar opcionalmente a la función del sistema después de completar su trabajo.</span><span class="sxs-lookup"><span data-stu-id="76e92-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="76e92-131">Un *nivel de compatibilidad* o un *modo* contiene una o varias correcciones de compatibilidad y marcas.</span><span class="sxs-lookup"><span data-stu-id="76e92-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76e92-132">En esta sección</span><span class="sxs-lookup"><span data-stu-id="76e92-132">In this section</span></span>

-   [<span data-ttu-id="76e92-133">**datos de APPHELP \_**</span><span class="sxs-lookup"><span data-stu-id="76e92-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="76e92-134">**ATTRINFO**</span><span class="sxs-lookup"><span data-stu-id="76e92-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="76e92-135">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="76e92-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="76e92-136">**BUSCAR \_ información**</span><span class="sxs-lookup"><span data-stu-id="76e92-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="76e92-137">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="76e92-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="76e92-138">**tipo de ruta de acceso \_**</span><span class="sxs-lookup"><span data-stu-id="76e92-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="76e92-139">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="76e92-140">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="76e92-141">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="76e92-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="76e92-142">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="76e92-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="76e92-143">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="76e92-144">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="76e92-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="76e92-145">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="76e92-146">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="76e92-147">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="76e92-148">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="76e92-149">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="76e92-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="76e92-150">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="76e92-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="76e92-151">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="76e92-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="76e92-152">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="76e92-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="76e92-153">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="76e92-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="76e92-154">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="76e92-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="76e92-155">**SdbGetIndex**</span><span class="sxs-lookup"><span data-stu-id="76e92-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="76e92-156">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="76e92-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="76e92-157">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="76e92-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="76e92-158">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="76e92-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="76e92-159">**SdbGetTagFromTagID**</span><span class="sxs-lookup"><span data-stu-id="76e92-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="76e92-160">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="76e92-161">**SdbIsStandardDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="76e92-162">**SdbMakeIndexKeyFromString**</span><span class="sxs-lookup"><span data-stu-id="76e92-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="76e92-163">**SdbOpenApphelpDetailsDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="76e92-164">**SdbOpenApphelpResourceFile**</span><span class="sxs-lookup"><span data-stu-id="76e92-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="76e92-165">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="76e92-166">**SdbQueryDataExTagID**</span><span class="sxs-lookup"><span data-stu-id="76e92-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="76e92-167">**SDBQUERYRESULT**</span><span class="sxs-lookup"><span data-stu-id="76e92-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="76e92-168">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="76e92-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="76e92-169">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="76e92-170">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="76e92-171">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="76e92-172">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="76e92-173">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="76e92-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="76e92-174">**SdbReleaseDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="76e92-175">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="76e92-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="76e92-176">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="76e92-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="76e92-177">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="76e92-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="76e92-178">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="76e92-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="76e92-179">**SdbTagToString**</span><span class="sxs-lookup"><span data-stu-id="76e92-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="76e92-180">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="76e92-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="76e92-181">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="76e92-182">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="76e92-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="76e92-183">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="76e92-184">**SdbWriteNULLTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="76e92-185">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="76e92-186">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="76e92-187">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="76e92-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="76e92-188">**Tipos de bases de datos de Shim**</span><span class="sxs-lookup"><span data-stu-id="76e92-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="76e92-189">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="76e92-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="76e92-190">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="76e92-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="76e92-191">**Tipos de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="76e92-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="76e92-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="76e92-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="76e92-193">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="76e92-193">**TAGREF**</span></span>](tagref.md)

 

 



