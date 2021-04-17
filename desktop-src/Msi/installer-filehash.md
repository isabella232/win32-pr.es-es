---
description: El método FileHash del objeto Installer toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo. La información de hash de archivo se devuelve como un objeto de registro. Todo el hash de archivo de 128 bits se devuelve como campos de propiedades IntegerData de 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Instalador. FileHash (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653336"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="25825-105">Instalador. FileHash (método)</span><span class="sxs-lookup"><span data-stu-id="25825-105">Installer.FileHash method</span></span>

<span data-ttu-id="25825-106">El método **FileHash** del [**objeto Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo.</span><span class="sxs-lookup"><span data-stu-id="25825-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="25825-107">La información de hash de archivo se devuelve como un [**objeto de registro**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="25825-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="25825-108">Todo el hash de archivo de 128 bits se devuelve como campos de propiedades [**IntegerData**](record-integerdata.md) de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="25825-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="25825-109">Los valores devueltos en el [**objeto de registro**](record-object.md) se corresponden con los cuatro campos de la estructura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) devuelta por [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="25825-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="25825-110">La numeración de cuatro campos se basa en 1 en la [tabla MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="25825-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="25825-111">El campo 1 corresponde a la columna HashPart1.</span><span class="sxs-lookup"><span data-stu-id="25825-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="25825-112">El campo 2 corresponde a la columna HashPart2.</span><span class="sxs-lookup"><span data-stu-id="25825-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="25825-113">El campo 3 corresponde a la columna HashPart3.</span><span class="sxs-lookup"><span data-stu-id="25825-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="25825-114">El campo 4 corresponde a la columna HashPart4.</span><span class="sxs-lookup"><span data-stu-id="25825-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="25825-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25825-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="25825-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25825-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25825-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="25825-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="25825-118">Ruta de acceso al archivo al que se va a aplicar un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="25825-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="25825-119">*Opciones*</span><span class="sxs-lookup"><span data-stu-id="25825-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="25825-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="25825-120">Reserved for future use.</span></span>

<span data-ttu-id="25825-121">El valor de este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="25825-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25825-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25825-122">Return value</span></span>

<span data-ttu-id="25825-123">Si es correcto, este método devuelve un [**objeto de registro**](record-object.md) que contiene el hash del archivo.</span><span class="sxs-lookup"><span data-stu-id="25825-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="25825-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25825-124">Requirements</span></span>



| <span data-ttu-id="25825-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="25825-125">Requirement</span></span> | <span data-ttu-id="25825-126">Value</span><span class="sxs-lookup"><span data-stu-id="25825-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25825-127">Versión</span><span class="sxs-lookup"><span data-stu-id="25825-127">Version</span></span><br/> | <span data-ttu-id="25825-128">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="25825-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="25825-129">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25825-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="25825-130">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="25825-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="25825-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25825-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="25825-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25825-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="25825-133">IID</span><span class="sxs-lookup"><span data-stu-id="25825-133">IID</span></span><br/>     | <span data-ttu-id="25825-134">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="25825-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="25825-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="25825-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25825-136">Control de versiones de archivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="25825-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="25825-137">Administrar versiones y tamaños de archivo</span><span class="sxs-lookup"><span data-stu-id="25825-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="25825-138">Tabla MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="25825-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="25825-139">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="25825-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




