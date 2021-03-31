---
title: Mensaje de MCIWNDM_NOTIFYMEDIA (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYMEDIA notifica a la ventana primaria de una aplicación que el medio ha cambiado.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- Mensaje de MCIWNDM_NOTIFYMEDIA de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802012"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="fb070-104">MCIWNDM \_ NOTIFYMEDIA</span><span class="sxs-lookup"><span data-stu-id="fb070-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="fb070-105">El mensaje **MCIWNDM \_ NOTIFYMEDIA** notifica a la ventana primaria de una aplicación que el medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fb070-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="fb070-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb070-107"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="fb070-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="fb070-108">Identificador de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fb070-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="fb070-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="fb070-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="fb070-110">Puntero a una cadena terminada en null que contiene el nuevo nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fb070-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="fb070-111">Si el medio se está cerrando, especifica una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="fb070-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb070-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb070-112">Remarks</span></span>

<span data-ttu-id="fb070-113">Puede habilitar la notificación de cambios de medios especificando el estilo de ventana de MCIWNDF \_ NOTIFYMEDIA.</span><span class="sxs-lookup"><span data-stu-id="fb070-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb070-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb070-114">Requirements</span></span>



| <span data-ttu-id="fb070-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb070-115">Requirement</span></span> | <span data-ttu-id="fb070-116">Value</span><span class="sxs-lookup"><span data-stu-id="fb070-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb070-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb070-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb070-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fb070-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fb070-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb070-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb070-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb070-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fb070-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb070-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb070-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb070-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





