---
description: El método Import del objeto de base de datos importa una tabla de base de datos de un archivo de almacenamiento de texto, quitando cualquier tabla existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670794"
---
# <a name="databaseimport-method"></a><span data-ttu-id="c97d1-103">Database. Import (método)</span><span class="sxs-lookup"><span data-stu-id="c97d1-103">Database.Import method</span></span>

<span data-ttu-id="c97d1-104">El método **Import** del objeto de [**base de datos**](database-object.md) importa una tabla de base de datos de un archivo de almacenamiento de [texto](text-archive-files.md), quitando cualquier tabla existente.</span><span class="sxs-lookup"><span data-stu-id="c97d1-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c97d1-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="c97d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c97d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97d1-107">*path*</span><span class="sxs-lookup"><span data-stu-id="c97d1-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="c97d1-108">Carpeta requerida en la que está presente el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="c97d1-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="c97d1-109">*file*</span><span class="sxs-lookup"><span data-stu-id="c97d1-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="c97d1-110">Nombre necesario del archivo que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="c97d1-110">Required name of the file to be imported.</span></span> <span data-ttu-id="c97d1-111">Esto no incluye la carpeta, ya que se debe establecer en el objeto de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c97d1-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="c97d1-112">El nombre de la tabla se especifica en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c97d1-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97d1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c97d1-113">Return value</span></span>

<span data-ttu-id="c97d1-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c97d1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97d1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c97d1-115">Remarks</span></span>

<span data-ttu-id="c97d1-116">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c97d1-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97d1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97d1-117">Requirements</span></span>



| <span data-ttu-id="c97d1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97d1-118">Requirement</span></span> | <span data-ttu-id="c97d1-119">Value</span><span class="sxs-lookup"><span data-stu-id="c97d1-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d1-120">Versión</span><span class="sxs-lookup"><span data-stu-id="c97d1-120">Version</span></span><br/> | <span data-ttu-id="c97d1-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c97d1-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c97d1-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c97d1-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c97d1-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c97d1-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c97d1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c97d1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c97d1-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c97d1-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c97d1-126">IID</span><span class="sxs-lookup"><span data-stu-id="c97d1-126">IID</span></span><br/>     | <span data-ttu-id="c97d1-127">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c97d1-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="c97d1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c97d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97d1-129">**Base de datos**</span><span class="sxs-lookup"><span data-stu-id="c97d1-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="c97d1-130">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="c97d1-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




