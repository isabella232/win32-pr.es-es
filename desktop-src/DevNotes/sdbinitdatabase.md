---
description: Abre la base de datos de correcciones de compatibilidad.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495923"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="5b5cb-103">SdbInitDatabase función)</span><span class="sxs-lookup"><span data-stu-id="5b5cb-103">SdbInitDatabase function</span></span>

<span data-ttu-id="5b5cb-104">Abre la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b5cb-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="5b5cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b5cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5cb-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b5cb-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5cb-108">Este parámetro especifica el formato de la ruta de acceso en el parámetro *pszDatabasePath* .</span><span class="sxs-lookup"><span data-stu-id="5b5cb-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="5b5cb-109">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-109">It can be one of the following values.</span></span>



| <span data-ttu-id="5b5cb-110">Value</span><span class="sxs-lookup"><span data-stu-id="5b5cb-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="5b5cb-111">Significado</span><span class="sxs-lookup"><span data-stu-id="5b5cb-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="5b5cb-112"><dt>**HID \_ \_Rutas**</dt> de acceso de dos <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="5b5cb-113">Una ruta de acceso de estilo MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="5b5cb-114"><dt>**HID \_ BASE de datos \_ FULLPATH**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="5b5cb-115">Ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="5b5cb-116"><dt>**HID \_ NO \_ Database**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="5b5cb-117">Se omite el parámetro *pszDatabasePath* y no se abre ninguna base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="5b5cb-118"><dt>**HID \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0xF00F0000</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="5b5cb-119">Este parámetro especifica una base de datos predefinida.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="5b5cb-120">Se omite el parámetro *pszDatabasePath* .</span><span class="sxs-lookup"><span data-stu-id="5b5cb-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="5b5cb-121">Si *dwFlags* contiene **la \_ \_ \_ máscara de tipo de datos HID**, este parámetro también puede incluir uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="5b5cb-122">Value</span><span class="sxs-lookup"><span data-stu-id="5b5cb-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="5b5cb-123">Significado</span><span class="sxs-lookup"><span data-stu-id="5b5cb-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="5b5cb-124"><dt>**SDB \_ \_Corrección de \_ compatibilidad principal de base de datos**</dt> <dt>0x80030000</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="5b5cb-125">Base de datos de corrección de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="5b5cb-126"><dt>**SDB \_ \_ \_ MSI principal**</dt> de la base de datos <dt>0x80020000</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="5b5cb-127">Base de datos MSI.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="5b5cb-128"><dt>**SDB \_ \_ \_ Controladores principales de base de datos**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="5b5cb-129">Base de datos de controladores que se van a bloquear.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5b5cb-130">*pszDatabasePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b5cb-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5cb-131">Ruta de acceso a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-131">The path to the database.</span></span> <span data-ttu-id="5b5cb-132">Este parámetro puede ser **null** si el parámetro *dwFlags* especifica una base de datos predefinida.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b5cb-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b5cb-133">Return value</span></span>

<span data-ttu-id="5b5cb-134">La función devuelve un identificador a la base de datos abierta.</span><span class="sxs-lookup"><span data-stu-id="5b5cb-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5cb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5cb-135">Requirements</span></span>



| <span data-ttu-id="5b5cb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5cb-136">Requirement</span></span> | <span data-ttu-id="5b5cb-137">Value</span><span class="sxs-lookup"><span data-stu-id="5b5cb-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5cb-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5cb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5cb-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5b5cb-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5b5cb-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5cb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5cb-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b5cb-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5b5cb-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b5cb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5cb-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cb-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5cb-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b5cb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5cb-145">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="5b5cb-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="5b5cb-146">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="5b5cb-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="5b5cb-147">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="5b5cb-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="5b5cb-148">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="5b5cb-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




