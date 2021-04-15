---
description: Envía el mensaje especificado a una ventana o ventanas.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649586"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="08280-103">\_SendMessage, función</span><span class="sxs-lookup"><span data-stu-id="08280-103">\_SendMessage function</span></span>

<span data-ttu-id="08280-104">\[Esta función es un contenedor de la función **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="08280-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="08280-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="08280-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="08280-106">Las aplicaciones deben llamar a **SendMessage** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="08280-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="08280-107">Envía el mensaje especificado a una ventana o ventanas.</span><span class="sxs-lookup"><span data-stu-id="08280-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="08280-108">Vea [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="08280-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="08280-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08280-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="08280-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08280-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08280-111">*...*</span><span class="sxs-lookup"><span data-stu-id="08280-111">*...*</span></span> 
<span data-ttu-id="08280-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="08280-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="08280-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08280-113">Requirements</span></span>



| <span data-ttu-id="08280-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="08280-114">Requirement</span></span> | <span data-ttu-id="08280-115">Value</span><span class="sxs-lookup"><span data-stu-id="08280-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08280-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08280-116">DLL</span></span><br/> | <dl> <span data-ttu-id="08280-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08280-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08280-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="08280-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08280-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="08280-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
