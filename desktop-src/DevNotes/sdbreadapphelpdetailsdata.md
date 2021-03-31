---
Description: Recupera datos de la base de datos de detalles de apphelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996326"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="cbbe8-103">SdbReadApphelpDetailsData función)</span><span class="sxs-lookup"><span data-stu-id="cbbe8-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="cbbe8-104">Recupera datos de la base de datos de detalles de apphelp.</span><span class="sxs-lookup"><span data-stu-id="cbbe8-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbe8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbbe8-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="cbbe8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbbe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbbe8-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cbbe8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbbe8-108">Identificador de la base de datos de detalles de apphelp, apphelp. sdb.</span><span class="sxs-lookup"><span data-stu-id="cbbe8-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="cbbe8-109">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cbbe8-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbbe8-110">Una estructura de [**\_ datos APPHELP**](apphelp-data.md) .</span><span class="sxs-lookup"><span data-stu-id="cbbe8-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbbe8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbbe8-111">Return value</span></span>

<span data-ttu-id="cbbe8-112">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="cbbe8-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbbe8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbbe8-113">Requirements</span></span>



| <span data-ttu-id="cbbe8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbbe8-114">Requirement</span></span> | <span data-ttu-id="cbbe8-115">Value</span><span class="sxs-lookup"><span data-stu-id="cbbe8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbbe8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbbe8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cbbe8-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cbbe8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cbbe8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbbe8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cbbe8-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbbe8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cbbe8-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbbe8-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbbe8-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbbe8-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




