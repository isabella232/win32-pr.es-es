---
description: El método OpenDatabase del objeto Installer abre una base de datos existente o crea una nueva, devolviendo un objeto Database. Genera un error si el objeto Database no se puede crear y abrir correctamente.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Método Installer.OpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492274"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="5f21c-104">Método Installer.OpenDatabase</span><span class="sxs-lookup"><span data-stu-id="5f21c-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="5f21c-105">El **método OpenDatabase** del objeto [**Installer**](installer-object.md) abre una base de datos existente o crea una nueva, devolviendo un objeto [**Database.**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="5f21c-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="5f21c-106">Genera un error si el objeto **Database** no se puede crear y abrir correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f21c-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f21c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f21c-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="5f21c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f21c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f21c-109">*name*</span><span class="sxs-lookup"><span data-stu-id="5f21c-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="5f21c-110">Cadena necesaria que contiene el nombre de ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f21c-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="5f21c-111">Si se proporciona una cadena vacía, se crea una base de datos temporal que no se conserva.</span><span class="sxs-lookup"><span data-stu-id="5f21c-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="5f21c-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="5f21c-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="5f21c-113">Parámetro de la lista siguiente o una cadena que contiene el nombre de ruta de acceso del nuevo archivo de base de datos de salida en el que se va a escribir tras la confirmación.</span><span class="sxs-lookup"><span data-stu-id="5f21c-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="5f21c-114">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5f21c-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="5f21c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5f21c-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="5f21c-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="5f21c-117">Abre una base de datos de solo lectura, sin cambios persistentes.</span><span class="sxs-lookup"><span data-stu-id="5f21c-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="5f21c-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="5f21c-119">Abre una base de datos de lectura y escritura en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="5f21c-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="5f21c-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="5f21c-121">Abre una base de datos de lectura y escritura directa sin transacción.</span><span class="sxs-lookup"><span data-stu-id="5f21c-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="5f21c-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="5f21c-123">Crea una nueva base de datos, lectura y escritura en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="5f21c-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="5f21c-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="5f21c-125">Crea una nueva base de datos, lectura y escritura en modo directo.</span><span class="sxs-lookup"><span data-stu-id="5f21c-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="5f21c-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="5f21c-127">Abre una base de datos para ver los archivos de script anunciados, como los archivos generados por [**el método CreateAdvertiseScript.**](installer-createadvertisescript.md)</span><span class="sxs-lookup"><span data-stu-id="5f21c-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="5f21c-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="5f21c-129">Agrega esta marca para indicar un archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="5f21c-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f21c-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f21c-130">Return value</span></span>

<span data-ttu-id="5f21c-131">Objeto [**Database**](database-object.md) que representa la base de datos existente o nueva del instalador que se abrió.</span><span class="sxs-lookup"><span data-stu-id="5f21c-131">A [**Database**](database-object.md) object that represents the existing or new installer database that was opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f21c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f21c-132">Remarks</span></span>

<span data-ttu-id="5f21c-133">Cuando se abre una base de datos como salida de otra base de datos, el flujo de información de resumen de la base de datos de salida es realmente un reflejo de solo lectura de la base de datos original y, por tanto, no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="5f21c-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="5f21c-134">Además, no se conserva con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f21c-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="5f21c-135">Para crear o modificar la información de resumen de la base de datos de salida, debe cerrarse y volver a abrirse.</span><span class="sxs-lookup"><span data-stu-id="5f21c-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="5f21c-136">Para realizar y guardar los cambios en una base de datos, abra primero la base de datos en la transacción (msiOpenDatabaseModeTransact), cree (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o en modo directo (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="5f21c-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="5f21c-137">Después de realizar los cambios, llame siempre al [**método Commit**](database-commit.md) antes de cerrar el identificador de base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f21c-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="5f21c-138">El **método Commit** vacía todos los búferes.</span><span class="sxs-lookup"><span data-stu-id="5f21c-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="5f21c-139">Llame siempre al [**método Commit**](database-commit.md) en una base de datos que se haya abierto en modo directo (msiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) antes de cerrar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f21c-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="5f21c-140">Si no lo hace, puede dañar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5f21c-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="5f21c-141">Dado que **el método OpenDatabase** inicia el acceso a la base de datos, no se puede usar con una instalación en ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f21c-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="5f21c-142">Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)</span><span class="sxs-lookup"><span data-stu-id="5f21c-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f21c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f21c-143">Requirements</span></span>



| <span data-ttu-id="5f21c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f21c-144">Requirement</span></span> | <span data-ttu-id="5f21c-145">Value</span><span class="sxs-lookup"><span data-stu-id="5f21c-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f21c-146">Versión</span><span class="sxs-lookup"><span data-stu-id="5f21c-146">Version</span></span><br/> | <span data-ttu-id="5f21c-147">Windows Installer 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f21c-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5f21c-148">Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5f21c-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5f21c-149">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f21c-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5f21c-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f21c-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f21c-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f21c-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5f21c-152">IID</span><span class="sxs-lookup"><span data-stu-id="5f21c-152">IID</span></span><br/>     | <span data-ttu-id="5f21c-153">IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046</span><span class="sxs-lookup"><span data-stu-id="5f21c-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




