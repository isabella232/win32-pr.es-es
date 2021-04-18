---
description: Envía los mensajes enviados entrantes, comprueba la cola de mensajes de subprocesos en busca de un mensaje expuesto y recupera el mensaje (si existe alguno).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649587"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="c9ad0-103">\_PeekMessage (función)</span><span class="sxs-lookup"><span data-stu-id="c9ad0-103">\_PeekMessage function</span></span>

<span data-ttu-id="c9ad0-104">\[Esta función es un contenedor de la función **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="c9ad0-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="c9ad0-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c9ad0-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="c9ad0-106">Las aplicaciones deben llamar a **PeekMessage** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="c9ad0-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="c9ad0-107">Envía los mensajes enviados entrantes, comprueba la cola de mensajes de subprocesos en busca de un mensaje expuesto y recupera el mensaje (si existe alguno).</span><span class="sxs-lookup"><span data-stu-id="c9ad0-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="c9ad0-108">Consulte [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="c9ad0-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ad0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9ad0-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="c9ad0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9ad0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ad0-111">*...*</span><span class="sxs-lookup"><span data-stu-id="c9ad0-111">*...*</span></span> 
<span data-ttu-id="c9ad0-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c9ad0-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c9ad0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9ad0-113">Requirements</span></span>



| <span data-ttu-id="c9ad0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ad0-114">Requirement</span></span> | <span data-ttu-id="c9ad0-115">Value</span><span class="sxs-lookup"><span data-stu-id="c9ad0-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ad0-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9ad0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="c9ad0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9ad0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ad0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9ad0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ad0-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="c9ad0-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
