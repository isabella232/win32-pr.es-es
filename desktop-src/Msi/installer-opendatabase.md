---
description: El método OpenDatabase del objeto Installer abre una base de datos existente o crea una nueva, y devuelve un objeto de base de datos. Genera un error si el objeto de base de datos no se puede crear y abrir correctamente.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase (método)
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
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653324"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="02e07-104">Installer. OpenDatabase (método)</span><span class="sxs-lookup"><span data-stu-id="02e07-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="02e07-105">El método **OpenDatabase** del objeto [**Installer**](installer-object.md) abre una base de datos existente o crea una nueva, y devuelve un objeto de [**base de datos**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="02e07-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="02e07-106">Genera un error si el objeto de **base de datos** no se puede crear y abrir correctamente.</span><span class="sxs-lookup"><span data-stu-id="02e07-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e07-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02e07-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="02e07-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02e07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e07-109">*name*</span><span class="sxs-lookup"><span data-stu-id="02e07-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="02e07-110">Cadena requerida que contiene el nombre de la ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02e07-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="02e07-111">Si se proporciona una cadena vacía, se crea una base de datos temporal que no se conserva.</span><span class="sxs-lookup"><span data-stu-id="02e07-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="02e07-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="02e07-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="02e07-113">Un parámetro de la lista siguiente o una cadena que contiene el nombre de la ruta de acceso del nuevo archivo de base de datos de salida que se va a escribir en el momento de la confirmación.</span><span class="sxs-lookup"><span data-stu-id="02e07-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="02e07-114">Parámetro</span><span class="sxs-lookup"><span data-stu-id="02e07-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="02e07-115">Significado</span><span class="sxs-lookup"><span data-stu-id="02e07-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="02e07-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="02e07-117">Abre una base de datos de solo lectura, sin cambios persistentes.</span><span class="sxs-lookup"><span data-stu-id="02e07-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="02e07-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="02e07-119">Abre una base de datos de lectura/escritura en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="02e07-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="02e07-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="02e07-121">Abre una base de datos directa de lectura/escritura sin transacción.</span><span class="sxs-lookup"><span data-stu-id="02e07-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="02e07-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="02e07-123">Crea una nueva base de datos, modo de lectura y escritura de Transact-is.</span><span class="sxs-lookup"><span data-stu-id="02e07-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="02e07-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="02e07-125">Crea una nueva base de datos, modo directo de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="02e07-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="02e07-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="02e07-127">Abre una base de datos para ver los archivos de script de anuncio, como los archivos generados por el método [**CreateAdvertiseScript**](installer-createadvertisescript.md) .</span><span class="sxs-lookup"><span data-stu-id="02e07-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="02e07-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="02e07-129">Agrega esta marca para indicar un archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="02e07-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e07-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02e07-130">Return value</span></span>

<span data-ttu-id="02e07-131">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="02e07-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e07-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02e07-132">Remarks</span></span>

<span data-ttu-id="02e07-133">Cuando una base de datos se abre como la salida de otra base de datos, la secuencia de información de Resumen de la base de datos de salida es realmente un reflejo de solo lectura de la base de datos original y, por tanto, no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="02e07-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="02e07-134">Además, no se conserva con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02e07-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="02e07-135">Para crear o modificar la información de Resumen de la base de datos de salida, se debe cerrar y volver a abrir.</span><span class="sxs-lookup"><span data-stu-id="02e07-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="02e07-136">Para realizar y guardar cambios en una base de datos, abra primero la base de datos en el modo de transacción (msiOpenDatabaseModeTransact), cree (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o Direct (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="02e07-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="02e07-137">Después de realizar los cambios, llame siempre al método [**commit**](database-commit.md) antes de cerrar el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02e07-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="02e07-138">El método **commit** vacía todos los búferes.</span><span class="sxs-lookup"><span data-stu-id="02e07-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="02e07-139">Llame siempre al método [**commit**](database-commit.md) en una base de datos que se haya abierto en modo directo (MsiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) antes de cerrar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02e07-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="02e07-140">Si no lo hace, puede dañar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02e07-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="02e07-141">Dado que el método **OpenDatabase** inicia el acceso a la base de datos, no se puede usar con una instalación en ejecución.</span><span class="sxs-lookup"><span data-stu-id="02e07-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="02e07-142">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="02e07-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e07-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e07-143">Requirements</span></span>



| <span data-ttu-id="02e07-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e07-144">Requirement</span></span> | <span data-ttu-id="02e07-145">Value</span><span class="sxs-lookup"><span data-stu-id="02e07-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e07-146">Versión</span><span class="sxs-lookup"><span data-stu-id="02e07-146">Version</span></span><br/> | <span data-ttu-id="02e07-147">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02e07-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02e07-148">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02e07-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02e07-149">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="02e07-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="02e07-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02e07-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="02e07-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e07-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="02e07-152">IID</span><span class="sxs-lookup"><span data-stu-id="02e07-152">IID</span></span><br/>     | <span data-ttu-id="02e07-153">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="02e07-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




