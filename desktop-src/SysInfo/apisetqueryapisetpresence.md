---
description: Esta API está pensada solo para uso interno y no debe usarse en el código.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Función ApiSetQueryApiSetPresence (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669980"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="00d4e-103">ApiSetQueryApiSetPresence función)</span><span class="sxs-lookup"><span data-stu-id="00d4e-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="00d4e-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="00d4e-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="00d4e-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="00d4e-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="00d4e-106">Esta API está pensada solo para uso interno y no debe usarse en el código.</span><span class="sxs-lookup"><span data-stu-id="00d4e-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d4e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00d4e-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="00d4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00d4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d4e-109">*Espacio de nombres* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00d4e-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="00d4e-110">*Presente* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00d4e-110">*Present* \[out\]</span></span>
<span data-ttu-id="00d4e-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="00d4e-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="00d4e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d4e-112">Requirements</span></span>



| <span data-ttu-id="00d4e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d4e-113">Requirement</span></span> | <span data-ttu-id="00d4e-114">Value</span><span class="sxs-lookup"><span data-stu-id="00d4e-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d4e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d4e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00d4e-116">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="00d4e-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="00d4e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d4e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00d4e-118">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="00d4e-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="00d4e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00d4e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d4e-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d4e-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="00d4e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00d4e-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="00d4e-122"><dt>API-MS-WIN-Core-apiquery-L1. lib; </dt> <dt>API-MS-WIN-Core-apiquery-L1-1 -0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00d4e-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="00d4e-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00d4e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d4e-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d4e-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




