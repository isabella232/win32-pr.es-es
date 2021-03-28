---
description: Carga una lista de cadenas en la lista de elementos usados más recientemente (MRU) del registro.
title: 'IACLCustomMRU:: Initialize (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997684"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="bf34a-103">IACLCustomMRU:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="bf34a-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="bf34a-104">Carga una lista de cadenas en la lista de elementos usados más recientemente (MRU) del registro.</span><span class="sxs-lookup"><span data-stu-id="bf34a-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf34a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf34a-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="bf34a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf34a-107">*pwszMRURegKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf34a-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf34a-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bf34a-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="bf34a-109">Un puntero a un búfer que contiene la clave del registro que contiene las cadenas para la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="bf34a-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="bf34a-110">*dwMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf34a-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf34a-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bf34a-111">Type: **DWORD**</span></span>

<span data-ttu-id="bf34a-112">Número máximo de entradas que se pueden tomar de *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="bf34a-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf34a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf34a-113">Return value</span></span>

<span data-ttu-id="bf34a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf34a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bf34a-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bf34a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf34a-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf34a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf34a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf34a-117">Requirements</span></span>



| <span data-ttu-id="bf34a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf34a-118">Requirement</span></span> | <span data-ttu-id="bf34a-119">Value</span><span class="sxs-lookup"><span data-stu-id="bf34a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf34a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf34a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf34a-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bf34a-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bf34a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf34a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf34a-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf34a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




