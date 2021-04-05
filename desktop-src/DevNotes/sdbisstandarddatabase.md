---
description: Determina si la base de datos especificada es una de las bases de datos estándar (SysMain, apphelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080089"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="f0c50-103">SdbIsStandardDatabase función)</span><span class="sxs-lookup"><span data-stu-id="f0c50-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="f0c50-104">Determina si la base de datos especificada es una de las bases de datos estándar (SysMain, apphelp, Drvmain o Msimain).</span><span class="sxs-lookup"><span data-stu-id="f0c50-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c50-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0c50-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="f0c50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0c50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c50-107">*GuidDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0c50-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c50-108">GUID para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f0c50-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c50-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0c50-109">Return value</span></span>

<span data-ttu-id="f0c50-110">La función devuelve **true** si el GUID representa una base de datos estándar o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f0c50-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c50-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c50-111">Requirements</span></span>



| <span data-ttu-id="f0c50-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c50-112">Requirement</span></span> | <span data-ttu-id="f0c50-113">Value</span><span class="sxs-lookup"><span data-stu-id="f0c50-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c50-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c50-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c50-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0c50-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0c50-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c50-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c50-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0c50-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f0c50-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0c50-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c50-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c50-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




