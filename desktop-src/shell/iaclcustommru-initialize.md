---
description: Carga una lista de cadenas en la lista de mru usada más recientemente desde el registro.
title: IACLCustomMRU::Initialize (Método)
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
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841236"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="44933-103">IACLCustomMRU::Initialize (Método)</span><span class="sxs-lookup"><span data-stu-id="44933-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="44933-104">Carga una lista de cadenas en la lista de mru usada más recientemente desde el registro.</span><span class="sxs-lookup"><span data-stu-id="44933-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="44933-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44933-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="44933-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44933-107">*pwszMRURegKey* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="44933-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44933-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="44933-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="44933-109">Puntero a un búfer que contiene la clave del Registro que contiene las cadenas de la lista de MRU.</span><span class="sxs-lookup"><span data-stu-id="44933-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="44933-110">*dwMax* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="44933-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44933-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="44933-111">Type: **DWORD**</span></span>

<span data-ttu-id="44933-112">Número máximo de entradas que se pueden tomar de *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="44933-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44933-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44933-113">Return value</span></span>

<span data-ttu-id="44933-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="44933-114">Type: **HRESULT**</span></span>

<span data-ttu-id="44933-115">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="44933-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44933-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="44933-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44933-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44933-117">Requirements</span></span>



| <span data-ttu-id="44933-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="44933-118">Requirement</span></span> | <span data-ttu-id="44933-119">Value</span><span class="sxs-lookup"><span data-stu-id="44933-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44933-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44933-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44933-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="44933-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="44933-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44933-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44933-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="44933-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




