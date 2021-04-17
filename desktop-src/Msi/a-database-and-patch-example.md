---
description: Una aplicación puede usar la función MsiOpenDatabase para abrir una base de datos de instalación nueva o existente (archivo. msi) o un paquete de revisión (archivo. msp). La aplicación comprueba el valor devuelto de MsiOpenDatabase antes de utilizar el identificador de base de datos.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Un ejemplo de base de datos y revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667075"
---
# <a name="a-database-and-patch-example"></a><span data-ttu-id="c40cf-103">Un ejemplo de base de datos y revisión</span><span class="sxs-lookup"><span data-stu-id="c40cf-103">A Database and Patch Example</span></span>

<span data-ttu-id="c40cf-104">Una aplicación puede usar la función [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir una base de datos de instalación nueva o existente (archivo. msi) o un paquete de revisión (archivo. msp). La aplicación comprueba el valor devuelto de **MsiOpenDatabase** antes de utilizar el identificador de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c40cf-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="c40cf-105">En los ejemplos siguientes se usan las variables de tipo **PMSIHANDLE** definidas en MSI. h.</span><span class="sxs-lookup"><span data-stu-id="c40cf-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="c40cf-106">Se recomienda usar el tipo **PMSIHANDLE** porque el instalador cierra los objetos **PMSIHANDLE** cuando salen del ámbito, mientras que la aplicación debe cerrar los objetos **MSIHANDLE** llamando a [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span><span class="sxs-lookup"><span data-stu-id="c40cf-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="c40cf-107">Para obtener más información, consulte la sección [uso de PMSIHANDLE en lugar de Handle](windows-installer-best-practices.md) en el [Windows Installer procedimientos recomendados](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="c40cf-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="c40cf-108">En el ejemplo siguiente se abre una base de datos, sample.msi, solo para lectura.</span><span class="sxs-lookup"><span data-stu-id="c40cf-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="c40cf-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) se ejecuta solo si sample.msi existe en el directorio c: \\ Test.</span><span class="sxs-lookup"><span data-stu-id="c40cf-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="c40cf-110">Cuando se realiza correctamente, el identificador de base de datos devuelto se puede usar para consultar los datos del paquete de instalación mediante [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) y [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span><span class="sxs-lookup"><span data-stu-id="c40cf-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="c40cf-111">En el ejemplo siguiente se abre la base de datos para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c40cf-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="c40cf-112">Si la aplicación llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), se guardan todos los cambios realizados en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c40cf-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="c40cf-113">Si la aplicación no llama a **MsiDatabaseCommit**, no se realiza ningún cambio en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c40cf-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="c40cf-114">En el ejemplo siguiente se toma una base de datos existente, se text.msi y se crea una nueva base de datos, newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="c40cf-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="c40cf-115">Cualquier cambio que se realice se puede guardar en la nueva base de datos mediante una llamada a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="c40cf-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="c40cf-116">La base de datos existente especificada en el parámetro *szDatabasePath* no cambia.</span><span class="sxs-lookup"><span data-stu-id="c40cf-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="c40cf-117">En el ejemplo siguiente se abre un paquete de revisión de Windows Installer (archivo. msp) para lectura solamente.</span><span class="sxs-lookup"><span data-stu-id="c40cf-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="c40cf-118">El identificador de revisión devuelto se puede usar para determinar los contenedores y los subalmacenamientos de transformación incluidos en el paquete de revisión mediante consultas en las tablas [ \_ streams](-streams-table.md) y [ \_ Storages](-storages-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c40cf-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="c40cf-119">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="c40cf-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="c40cf-120">A partir de Windows Installer 3,0, la aplicación puede consultar la [tabla MsiPatchSequence](msipatchsequence-table.md) presente en un paquete de revisión que utiliza la nueva información de secuencia de revisión.</span><span class="sxs-lookup"><span data-stu-id="c40cf-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



