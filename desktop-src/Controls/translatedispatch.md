---
title: Función de devolución de llamada TranslateDispatch
description: Lo usa el cliente de la función DoReaderMode para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana de modo lector. Se trata de una función de devolución de llamada definida por la aplicación.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch (función de devolución de llamada) controles de Windows
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996281"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="8e7ca-105">Función de devolución de llamada TranslateDispatch</span><span class="sxs-lookup"><span data-stu-id="8e7ca-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="8e7ca-106">\[*TranslateDispatch* está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8e7ca-107">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="8e7ca-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8e7ca-108">Lo usa el cliente de la función [**DoReaderMode**](doreadermode.md) para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana de modo lector.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="8e7ca-109">Se trata de una función de devolución de llamada definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7ca-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e7ca-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="8e7ca-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e7ca-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e7ca-112">*lpmsg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e7ca-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e7ca-113">Tipo: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="8e7ca-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="8e7ca-114">Puntero a una estructura [_ *MSG* \*](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje interceptado.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e7ca-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e7ca-115">Return value</span></span>

<span data-ttu-id="8e7ca-116">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8e7ca-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8e7ca-117">**True** si esta función controla el mensaje; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="8e7ca-118">Si es **false**, el mensaje se controla mediante la implementación del modo de lectura predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="8e7ca-119">Esa implementación controla el movimiento y los botones del mouse, así como las pulsaciones de teclas.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="8e7ca-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8e7ca-120">Examples</span></span>

<span data-ttu-id="8e7ca-121">En el siguiente ejemplo se describe una implementación de esta función.</span><span class="sxs-lookup"><span data-stu-id="8e7ca-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="8e7ca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e7ca-122">Requirements</span></span>



| <span data-ttu-id="8e7ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e7ca-123">Requirement</span></span> | <span data-ttu-id="8e7ca-124">Value</span><span class="sxs-lookup"><span data-stu-id="8e7ca-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e7ca-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e7ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7ca-126">Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e7ca-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8e7ca-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e7ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7ca-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e7ca-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

