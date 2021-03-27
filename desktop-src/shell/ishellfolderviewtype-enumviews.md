---
description: Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista ampliada.
title: 'IShellFolderViewType:: EnumViews (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997280"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="5b1a3-103">IShellFolderViewType:: EnumViews (método)</span><span class="sxs-lookup"><span data-stu-id="5b1a3-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="5b1a3-104">Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista ampliada.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b1a3-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="5b1a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b1a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1a3-107">*grfFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b1a3-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1a3-108">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="5b1a3-108">Type: **ULONG**</span></span>

<span data-ttu-id="5b1a3-109">Marcas que indican qué elementos se van a incluir en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="5b1a3-110">Para obtener una lista de los valores posibles, vea el tipo enumerado [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) .</span><span class="sxs-lookup"><span data-stu-id="5b1a3-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="5b1a3-111">Este parámetro se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b1a3-112">*ppenum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5b1a3-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1a3-113">Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="5b1a3-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="5b1a3-114">Dirección de una variable de puntero de tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) que recibe el enumerador.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1a3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b1a3-115">Return value</span></span>

<span data-ttu-id="5b1a3-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b1a3-116">Type: **HRESULT**</span></span>

<span data-ttu-id="5b1a3-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b1a3-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b1a3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b1a3-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b1a3-119">Remarks</span></span>

<span data-ttu-id="5b1a3-120">Las vistas se representan al usuario como carpetas ocultas fuera del directorio raíz (representado por PIDL).</span><span class="sxs-lookup"><span data-stu-id="5b1a3-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="5b1a3-121">Siempre que sea necesario, la vista predeterminada (fuera de la carpeta raíz) se representa como **null**, o está vacía, PIDL.</span><span class="sxs-lookup"><span data-stu-id="5b1a3-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1a3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b1a3-122">Requirements</span></span>



| <span data-ttu-id="5b1a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b1a3-123">Requirement</span></span> | <span data-ttu-id="5b1a3-124">Value</span><span class="sxs-lookup"><span data-stu-id="5b1a3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1a3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b1a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5b1a3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b1a3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5b1a3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b1a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5b1a3-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b1a3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5b1a3-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b1a3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b1a3-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b1a3-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




