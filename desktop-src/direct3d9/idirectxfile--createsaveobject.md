---
description: Crea un objeto Save. En desuso.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile:: CreateSaveObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670255"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="5530f-104">IDirectXFile:: CreateSaveObject (método)</span><span class="sxs-lookup"><span data-stu-id="5530f-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="5530f-105">Crea un objeto Save.</span><span class="sxs-lookup"><span data-stu-id="5530f-105">Creates a save object.</span></span> <span data-ttu-id="5530f-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="5530f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5530f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5530f-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="5530f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5530f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5530f-109">*szFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5530f-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5530f-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5530f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5530f-111">Puntero al nombre del archivo que se va a usar para guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="5530f-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="5530f-112">*dwFileFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5530f-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5530f-113">Tipo: **[ **DXFILEFORMAT**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="5530f-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="5530f-114">Indica el formato que se va a utilizar al guardar el archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="5530f-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="5530f-115">Este valor puede ser una de las \_ marcas DXFILEFORMAT XXX en las [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="5530f-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="5530f-116">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5530f-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5530f-117">*ppSaveObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5530f-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5530f-118">Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="5530f-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="5530f-119">Dirección de un puntero a una interfaz [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) que representa el objeto guardado que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="5530f-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5530f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5530f-120">Return value</span></span>

<span data-ttu-id="5530f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5530f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5530f-122">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5530f-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="5530f-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="5530f-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="5530f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5530f-124">Remarks</span></span>

<span data-ttu-id="5530f-125">Después de usar este método, use los métodos de la interfaz [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.</span><span class="sxs-lookup"><span data-stu-id="5530f-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="5530f-126">El valor predeterminado para el formato de archivo es DXFILEFORMAT \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="5530f-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="5530f-127">Los valores de formato de archivo se pueden combinar en un OR lógico para crear texto comprimido o archivos binarios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="5530f-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="5530f-128">Si se especifica un archivo como binario (0) y texto (1), se guardará como un archivo de texto porque no se puede distinguir el valor del valor de formato de archivo de texto (0 + 1 = 1).</span><span class="sxs-lookup"><span data-stu-id="5530f-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="5530f-129">Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y se comprimirá.</span><span class="sxs-lookup"><span data-stu-id="5530f-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="5530f-130">Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binario, por lo que en la mayoría de los casos querrá indicar binario y comprimido.</span><span class="sxs-lookup"><span data-stu-id="5530f-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="5530f-131">Si se establece un archivo que se va a comprimir sin especificar un formato, se generará un archivo comprimido binario.</span><span class="sxs-lookup"><span data-stu-id="5530f-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5530f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5530f-132">Requirements</span></span>



| <span data-ttu-id="5530f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5530f-133">Requirement</span></span> | <span data-ttu-id="5530f-134">Value</span><span class="sxs-lookup"><span data-stu-id="5530f-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5530f-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5530f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="5530f-136"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5530f-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5530f-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5530f-137">Library</span></span><br/> | <dl> <span data-ttu-id="5530f-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5530f-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5530f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5530f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5530f-140">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="5530f-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="5530f-141">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="5530f-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
