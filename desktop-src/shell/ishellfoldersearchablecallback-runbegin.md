---
description: Indica que se ha iniciado una búsqueda.
title: 'IShellFolderSearchableCallback:: RunBegin (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 2bef0f29486143f97f886c0d31ab456a070ed857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543110"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="04b58-103">IShellFolderSearchableCallback:: RunBegin (método)</span><span class="sxs-lookup"><span data-stu-id="04b58-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="04b58-104">Indica que se ha iniciado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="04b58-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04b58-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="04b58-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04b58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b58-107">*dwReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04b58-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b58-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="04b58-108">Type: **DWORD**</span></span>

<span data-ttu-id="04b58-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="04b58-109">Reserved.</span></span> <span data-ttu-id="04b58-110">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="04b58-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b58-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04b58-111">Return value</span></span>

<span data-ttu-id="04b58-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04b58-112">Type: **HRESULT**</span></span>

<span data-ttu-id="04b58-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="04b58-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04b58-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04b58-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b58-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04b58-115">Remarks</span></span>

<span data-ttu-id="04b58-116">Como respuesta a esta devolución de llamada, la aplicación puede habilitar el botón **Cancelar** , por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="04b58-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b58-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b58-117">Requirements</span></span>



| <span data-ttu-id="04b58-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b58-118">Requirement</span></span> | <span data-ttu-id="04b58-119">Value</span><span class="sxs-lookup"><span data-stu-id="04b58-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b58-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04b58-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04b58-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04b58-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04b58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04b58-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04b58-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04b58-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04b58-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b58-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b58-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




