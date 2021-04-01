---
title: Mensaje de TB_ADDBITMAP (commctrl. h)
description: Agrega una o más imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804129"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="a5ade-104">\_Mensaje ADDBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="a5ade-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="a5ade-105">Agrega una o más imágenes a la lista de imágenes de botón disponibles para una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="a5ade-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5ade-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ade-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5ade-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ade-108">Número de imágenes de botón en el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a5ade-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="a5ade-109">Si *lParam* especifica un mapa de bits definido por el sistema, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="a5ade-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a5ade-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5ade-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ade-111">Puntero a una estructura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) que contiene el identificador de un recurso de mapa de bits y el identificador de la instancia de módulo con el archivo ejecutable que contiene el recurso de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a5ade-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ade-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5ade-112">Return value</span></span>

<span data-ttu-id="a5ade-113">Devuelve el índice de la primera imagen nueva si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5ade-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ade-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5ade-114">Remarks</span></span>

<span data-ttu-id="a5ade-115">Si la barra de herramientas se creó mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , debe enviar el mensaje de [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de enviar **TB \_ ADDBITMAP**.</span><span class="sxs-lookup"><span data-stu-id="a5ade-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="a5ade-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5ade-116">Examples</span></span>

<span data-ttu-id="a5ade-117">En el ejemplo siguiente se crea un mapa de bits a partir de un recurso (IDB \_ BITMAP1), se asigna el color de fondo (negro en este caso) al color de la superficie del botón del sistema y se agrega a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="a5ade-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="a5ade-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5ade-118">Requirements</span></span>



| <span data-ttu-id="a5ade-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5ade-119">Requirement</span></span> | <span data-ttu-id="a5ade-120">Value</span><span class="sxs-lookup"><span data-stu-id="a5ade-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ade-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5ade-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ade-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5ade-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5ade-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5ade-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ade-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5ade-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5ade-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5ade-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ade-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5ade-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

