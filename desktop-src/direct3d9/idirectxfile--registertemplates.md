---
description: Registra plantillas personalizadas. En desuso.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'IDirectXFile:: RegisterTemplates (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670225"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="4e667-104">IDirectXFile:: RegisterTemplates (método)</span><span class="sxs-lookup"><span data-stu-id="4e667-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="4e667-105">Registra plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4e667-105">Registers custom templates.</span></span> <span data-ttu-id="4e667-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4e667-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e667-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e667-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="4e667-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e667-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e667-109">*pvData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e667-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e667-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e667-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e667-111">Puntero a un búfer que se compone de un archivo de DirectX en formato de texto o binario que contiene plantillas.</span><span class="sxs-lookup"><span data-stu-id="4e667-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="4e667-112">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e667-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e667-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e667-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e667-114">Tamaño del búfer al que apunta pvData, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4e667-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e667-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e667-115">Return value</span></span>

<span data-ttu-id="4e667-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e667-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e667-117">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e667-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4e667-118">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADVALUE, DXFILEERR \_ Nº.</span><span class="sxs-lookup"><span data-stu-id="4e667-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e667-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e667-119">Remarks</span></span>

<span data-ttu-id="4e667-120">El siguiente fragmento de código proporciona una llamada de ejemplo a **RegisterTemplates** y el contenido de ejemplo para el búfer al que apunta pvData.</span><span class="sxs-lookup"><span data-stu-id="4e667-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="4e667-121">Todas las plantillas deben especificar un nombre y un identificador único universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="4e667-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e667-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e667-122">Requirements</span></span>



| <span data-ttu-id="4e667-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e667-123">Requirement</span></span> | <span data-ttu-id="4e667-124">Value</span><span class="sxs-lookup"><span data-stu-id="4e667-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e667-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e667-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4e667-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e667-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e667-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e667-127">Library</span></span><br/> | <dl> <span data-ttu-id="4e667-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e667-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e667-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e667-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e667-130">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="4e667-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
