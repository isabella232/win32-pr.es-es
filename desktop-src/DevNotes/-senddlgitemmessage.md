---
description: Envía un mensaje al control especificado en un cuadro de diálogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660293"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="6a773-103">\_SendDlgItemMessage función)</span><span class="sxs-lookup"><span data-stu-id="6a773-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="6a773-104">\[Esta función es un contenedor de la función **SendDlgItemMessage** .</span><span class="sxs-lookup"><span data-stu-id="6a773-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="6a773-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="6a773-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="6a773-106">Las aplicaciones deben llamar a **SendDlgItemMessage** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="6a773-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="6a773-107">Envía un mensaje al control especificado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6a773-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="6a773-108">Vea [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="6a773-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a773-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a773-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="6a773-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a773-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a773-111">*...*</span><span class="sxs-lookup"><span data-stu-id="6a773-111">*...*</span></span> 
<span data-ttu-id="6a773-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6a773-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6a773-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a773-113">Requirements</span></span>



| <span data-ttu-id="6a773-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a773-114">Requirement</span></span> | <span data-ttu-id="6a773-115">Value</span><span class="sxs-lookup"><span data-stu-id="6a773-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a773-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a773-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6a773-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a773-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a773-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a773-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a773-119">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="6a773-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
