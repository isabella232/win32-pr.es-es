---
description: Establece los puntos de los objetos seleccionados actualmente en el objeto de datos en los comandos de copiar y cortar. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_SETPOINTS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279389"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="55ad7-104">SFVM \_ SETPOINTS</span><span class="sxs-lookup"><span data-stu-id="55ad7-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="55ad7-105">Establece los puntos de los objetos seleccionados actualmente en el objeto de datos en los comandos de **copiar** y **cortar** .</span><span class="sxs-lookup"><span data-stu-id="55ad7-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="55ad7-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="55ad7-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="55ad7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55ad7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ad7-108">*pdtobj* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55ad7-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="55ad7-109">Un puntero a un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> de los comandos de **copiar** y **cortar** .</span><span class="sxs-lookup"><span data-stu-id="55ad7-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ad7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55ad7-110">Return value</span></span>

<span data-ttu-id="55ad7-111">Siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="55ad7-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ad7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55ad7-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="55ad7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55ad7-113">Requirements</span></span>



| <span data-ttu-id="55ad7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ad7-114">Requirement</span></span> | <span data-ttu-id="55ad7-115">Value</span><span class="sxs-lookup"><span data-stu-id="55ad7-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55ad7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55ad7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="55ad7-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55ad7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="55ad7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55ad7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="55ad7-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55ad7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55ad7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55ad7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="55ad7-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ad7-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
