---
description: El método Export del objeto Database copia la estructura y los datos de una tabla especificada en un archivo de almacenamiento de texto.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653488"
---
# <a name="databaseexport-method"></a><span data-ttu-id="13bcb-103">Database. Export (método)</span><span class="sxs-lookup"><span data-stu-id="13bcb-103">Database.Export method</span></span>

<span data-ttu-id="13bcb-104">El método **Export** del objeto [**Database**](database-object.md) copia la estructura y los datos de una tabla especificada en un [archivo de almacenamiento de texto](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="13bcb-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13bcb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13bcb-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="13bcb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13bcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bcb-107">*table*</span><span class="sxs-lookup"><span data-stu-id="13bcb-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="13bcb-108">Nombre necesario de la tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="13bcb-108">Required name of the database table.</span></span> <span data-ttu-id="13bcb-109">Distingue mayúsculas de minúsculas si se utiliza la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="13bcb-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="13bcb-110">*path*</span><span class="sxs-lookup"><span data-stu-id="13bcb-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="13bcb-111">Cadena requerida que es la ruta de acceso a la carpeta donde se coloca el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="13bcb-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="13bcb-112">*file*</span><span class="sxs-lookup"><span data-stu-id="13bcb-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="13bcb-113">Nombre necesario del archivo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="13bcb-113">Required name of the file to be created.</span></span> <span data-ttu-id="13bcb-114">Esto no incluye la carpeta, ya que se debe establecer en el objeto de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="13bcb-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bcb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13bcb-115">Return value</span></span>

<span data-ttu-id="13bcb-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13bcb-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bcb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13bcb-117">Remarks</span></span>

<span data-ttu-id="13bcb-118">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="13bcb-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bcb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13bcb-119">Requirements</span></span>



| <span data-ttu-id="13bcb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="13bcb-120">Requirement</span></span> | <span data-ttu-id="13bcb-121">Value</span><span class="sxs-lookup"><span data-stu-id="13bcb-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13bcb-122">Versión</span><span class="sxs-lookup"><span data-stu-id="13bcb-122">Version</span></span><br/> | <span data-ttu-id="13bcb-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="13bcb-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="13bcb-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13bcb-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="13bcb-125">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="13bcb-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="13bcb-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13bcb-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="13bcb-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bcb-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="13bcb-128">IID</span><span class="sxs-lookup"><span data-stu-id="13bcb-128">IID</span></span><br/>     | <span data-ttu-id="13bcb-129">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="13bcb-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




