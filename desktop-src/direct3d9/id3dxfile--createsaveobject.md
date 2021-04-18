---
description: Crea un objeto Save que se usará para guardar los datos en un archivo. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile:: CreateSaveObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718325"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="e0618-103">ID3DXFile:: CreateSaveObject (método)</span><span class="sxs-lookup"><span data-stu-id="e0618-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="e0618-104">Crea un objeto Save que se usará para guardar los datos en un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="e0618-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0618-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0618-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="e0618-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0618-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0618-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0618-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0618-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0618-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0618-109">Puntero al nombre del archivo que se va a usar para guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="e0618-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="e0618-110">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e0618-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0618-111">Tipo: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="e0618-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="e0618-112">Valor que especifica el nombre del archivo en el que se van a guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="e0618-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="e0618-113">Este valor puede ser una de las marcas de [opciones para guardar archivos](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0618-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="e0618-114">*dwFileFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0618-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0618-115">Tipo: **[D3DXF \_ FILEFORMAT](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="e0618-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="e0618-116">Indica el formato que se va a utilizar al guardar el archivo. x.</span><span class="sxs-lookup"><span data-stu-id="e0618-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="e0618-117">Este valor puede ser una de las marcas de [formatos de archivo](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0618-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="e0618-118">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e0618-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e0618-119">*ppSaveObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0618-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0618-120">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0618-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="e0618-121">Dirección de un puntero a una interfaz [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa el objeto guardado que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="e0618-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0618-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0618-122">Return value</span></span>

<span data-ttu-id="e0618-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0618-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0618-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0618-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e0618-125">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ Nº.</span><span class="sxs-lookup"><span data-stu-id="e0618-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0618-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0618-126">Remarks</span></span>

<span data-ttu-id="e0618-127">Después de usar este método, use los métodos de la interfaz [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) para crear objetos de datos y guardar plantillas o datos.</span><span class="sxs-lookup"><span data-stu-id="e0618-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="e0618-128">Para el formato de archivo guardado *dwFileFormat*, se debe especificar una de las marcas binarias, binarias heredadas o de texto en [formatos de archivo](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0618-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="e0618-129">El archivo se puede comprimir mediante el uso de la \_ marca D3DXF FILEFORMAT \_ comprimida opcional.</span><span class="sxs-lookup"><span data-stu-id="e0618-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="e0618-130">Los valores de formato de archivo se pueden combinar en un OR lógico para crear texto comprimido o archivos binarios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="e0618-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="e0618-131">Si indica que el formato de archivo debe ser texto y comprimido, el archivo se escribirá primero como texto y después se comprimirá.</span><span class="sxs-lookup"><span data-stu-id="e0618-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="e0618-132">Sin embargo, los archivos de texto comprimidos no son tan eficaces como los archivos de texto binario; en la mayoría de los casos, por lo tanto, querrá indicar binario y comprimido.</span><span class="sxs-lookup"><span data-stu-id="e0618-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0618-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0618-133">Requirements</span></span>



| <span data-ttu-id="e0618-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0618-134">Requirement</span></span> | <span data-ttu-id="e0618-135">Value</span><span class="sxs-lookup"><span data-stu-id="e0618-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0618-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0618-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e0618-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0618-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e0618-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0618-138">Library</span></span><br/> | <dl> <span data-ttu-id="e0618-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0618-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e0618-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0618-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0618-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="e0618-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="e0618-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="e0618-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
