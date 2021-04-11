---
description: Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Estructura DEVICEDIALOGDATA2 (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082673"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="cb539-103">Estructura DEVICEDIALOGDATA2</span><span class="sxs-lookup"><span data-stu-id="cb539-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="cb539-104">Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb539-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb539-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb539-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="cb539-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb539-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb539-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="cb539-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cb539-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-109">Especifica el tamaño de esta estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="cb539-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="cb539-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-111">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="cb539-111">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="cb539-112">Apunta a una interfaz [_ *IWiaItem2* \*](-wia-iwiaitem2.md) que representa el elemento raíz válido en el árbol de elementos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb539-112">Points to an [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="cb539-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cb539-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-115">Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cb539-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="cb539-116">Se puede establecer en cualquiera de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="cb539-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="cb539-117">Marca</span><span class="sxs-lookup"><span data-stu-id="cb539-117">Flag</span></span>                                 | <span data-ttu-id="cb539-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cb539-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb539-119">0</span><span class="sxs-lookup"><span data-stu-id="cb539-119">0</span></span>                                    | <span data-ttu-id="cb539-120">Comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cb539-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="cb539-121">\_cuadro de diálogo de dispositivo WIA \_ \_ \_ imagen única</span><span class="sxs-lookup"><span data-stu-id="cb539-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="cb539-122">Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo adquisición de imagen de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb539-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="cb539-123">cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común</span><span class="sxs-lookup"><span data-stu-id="cb539-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="cb539-124">Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cb539-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="cb539-125">Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cb539-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="cb539-126">Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="cb539-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="cb539-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="cb539-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-128">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="cb539-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-129">Especifica el identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cb539-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="cb539-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-131">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb539-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-132">Especifica el nombre de la carpeta donde se transfieren los archivos.</span><span class="sxs-lookup"><span data-stu-id="cb539-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="cb539-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-134">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb539-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-135">Especifica la plantilla de nombre de archivo que se va a usar para los archivos transferidos desde elementos WIA a la carpeta de destino designada por **bstrFolderName**.</span><span class="sxs-lookup"><span data-stu-id="cb539-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="cb539-136">Se puede crear un número arbitrario de nombres de archivo únicos anexando caracteres adicionales a la plantilla de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="cb539-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="cb539-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-138">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="cb539-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="cb539-139">Recibe el número de cadenas escritas en la matriz **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="cb539-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="cb539-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="cb539-141">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="cb539-141">Type: \**BSTR\** _</span></span>

</dd> <dd>

<span data-ttu-id="cb539-142">Puntero a una matriz de punteros BSTR.</span><span class="sxs-lookup"><span data-stu-id="cb539-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="cb539-143">Cada elemento de la matriz apunta a un BSTR que contiene el nombre de destino de un archivo que se ha transferido correctamente a la carpeta identificada por bstrFolderName.</span><span class="sxs-lookup"><span data-stu-id="cb539-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="cb539-144">El método debe asignar el almacenamiento de este miembro.</span><span class="sxs-lookup"><span data-stu-id="cb539-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="cb539-145">_ *ppWiaItem*\*</span><span class="sxs-lookup"><span data-stu-id="cb539-145">_ *ppWiaItem*\*</span></span>
</dt> <dd>

<span data-ttu-id="cb539-146">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="cb539-146">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="cb539-147">Puntero a la interfaz [_ *IWiaItem2* \*](-wia-iwiaitem2.md) del elemento WIA que transfiere los datos al archivo o los archivos nombrados en la matriz **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="cb539-147">Pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb539-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb539-148">Requirements</span></span>



| <span data-ttu-id="cb539-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb539-149">Requirement</span></span> | <span data-ttu-id="cb539-150">Value</span><span class="sxs-lookup"><span data-stu-id="cb539-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb539-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb539-151">Minimum supported client</span></span><br/> | <span data-ttu-id="cb539-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb539-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cb539-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb539-153">Minimum supported server</span></span><br/> | <span data-ttu-id="cb539-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb539-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb539-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb539-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb539-156"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb539-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




