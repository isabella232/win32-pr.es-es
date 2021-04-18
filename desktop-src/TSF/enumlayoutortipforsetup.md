---
title: EnumLayoutOrTipForSetup función)
description: Enumera las distribuciones de teclado instaladas y los servicios de texto de la interfaz de usuario del programa de instalación o OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup función de servicios de texto
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685950"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="53d57-104">EnumLayoutOrTipForSetup función)</span><span class="sxs-lookup"><span data-stu-id="53d57-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="53d57-105">Enumera las distribuciones de teclado instaladas y los servicios de texto de la interfaz de usuario del programa de instalación o OOBE.</span><span class="sxs-lookup"><span data-stu-id="53d57-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d57-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53d57-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="53d57-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53d57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d57-108">*langid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53d57-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d57-109">Identificador de idioma del elemento que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="53d57-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="53d57-110">*pLayoutOrTip* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53d57-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53d57-111">Puntero al búfer que recibe la matriz de estructuras LAYOUTORTIP.</span><span class="sxs-lookup"><span data-stu-id="53d57-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="53d57-112">Puede ser **null** para obtener el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="53d57-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="53d57-113">*uBufLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53d57-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d57-114">Longitud del búfer al que apunta *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="53d57-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="53d57-115">Se omite si *pLayoutOrTip* es **null**.</span><span class="sxs-lookup"><span data-stu-id="53d57-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="53d57-116">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53d57-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d57-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="53d57-117">Not used.</span></span> <span data-ttu-id="53d57-118">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53d57-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d57-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d57-119">Return value</span></span>

<span data-ttu-id="53d57-120">Si *pLayoutOrTip* es **null**, el número de elementos de teclado que están registrados en el sistema; de lo contrario, el número de elementos de teclado que se copian en *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="53d57-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="53d57-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53d57-121">Remarks</span></span>

<span data-ttu-id="53d57-122">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="53d57-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="53d57-123">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="53d57-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="53d57-124">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="53d57-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="53d57-125">La definición de LAYOUTORTIP es:</span><span class="sxs-lookup"><span data-stu-id="53d57-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="53d57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53d57-126">Requirements</span></span>



| <span data-ttu-id="53d57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d57-127">Requirement</span></span> | <span data-ttu-id="53d57-128">Value</span><span class="sxs-lookup"><span data-stu-id="53d57-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53d57-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53d57-129">Minimum supported client</span></span><br/> | <span data-ttu-id="53d57-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53d57-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="53d57-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53d57-131">Minimum supported server</span></span><br/> | <span data-ttu-id="53d57-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53d57-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="53d57-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53d57-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d57-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53d57-134"><dt>Input.dll</dt></span></span> </dl> |



 

