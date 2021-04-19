---
description: Finaliza el seguimiento.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: TermAsyncTrace función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650071"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="7f40d-103">TermAsyncTrace función)</span><span class="sxs-lookup"><span data-stu-id="7f40d-103">TermAsyncTrace function</span></span>

<span data-ttu-id="7f40d-104">Finaliza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7f40d-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f40d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f40d-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="7f40d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f40d-106">Parameters</span></span>

<span data-ttu-id="7f40d-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7f40d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f40d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f40d-108">Return value</span></span>

<span data-ttu-id="7f40d-109">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7f40d-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f40d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f40d-110">Remarks</span></span>

<span data-ttu-id="7f40d-111">Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el protocolo de transferencia de noticias en red (NNTP).</span><span class="sxs-lookup"><span data-stu-id="7f40d-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="7f40d-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7f40d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f40d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f40d-113">Requirements</span></span>



| <span data-ttu-id="7f40d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f40d-114">Requirement</span></span> | <span data-ttu-id="7f40d-115">Value</span><span class="sxs-lookup"><span data-stu-id="7f40d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f40d-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f40d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7f40d-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f40d-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
