---
description: Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta shell.
title: IShellFolderSearchable::InvalidateSearch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841696"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="902a4-103">IShellFolderSearchable::InvalidateSearch (método)</span><span class="sxs-lookup"><span data-stu-id="902a4-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="902a4-104">Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta shell.</span><span class="sxs-lookup"><span data-stu-id="902a4-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="902a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="902a4-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="902a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="902a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="902a4-107">*pidlSearch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="902a4-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="902a4-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="902a4-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="902a4-109">Puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) de la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="902a4-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="902a4-110">*pdwFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="902a4-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="902a4-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="902a4-111">Type: **DWORD\***</span></span>

<span data-ttu-id="902a4-112">No hay marcas definidas actualmente; se establece en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="902a4-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="902a4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="902a4-113">Return value</span></span>

<span data-ttu-id="902a4-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="902a4-114">Type: **HRESULT**</span></span>

<span data-ttu-id="902a4-115">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="902a4-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="902a4-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="902a4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="902a4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="902a4-117">Remarks</span></span>

<span data-ttu-id="902a4-118">Cuando se invalida una carpeta de búsqueda, puede realizar la limpieza de los recursos que ha usado.</span><span class="sxs-lookup"><span data-stu-id="902a4-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="902a4-119">El **método IShellFolderSearchable::InvalidateSearch** puede hacer que se cancele una búsqueda asincrónica y dará lugar a la versión final del objeto de interfaz [**IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md)</span><span class="sxs-lookup"><span data-stu-id="902a4-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="902a4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="902a4-120">Requirements</span></span>



| <span data-ttu-id="902a4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="902a4-121">Requirement</span></span> | <span data-ttu-id="902a4-122">Value</span><span class="sxs-lookup"><span data-stu-id="902a4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="902a4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="902a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="902a4-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="902a4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="902a4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="902a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="902a4-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="902a4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="902a4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="902a4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="902a4-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="902a4-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




