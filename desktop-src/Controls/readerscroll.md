---
title: Función de devolución de llamada ReaderScroll
description: Función de devolución de llamada definida por la aplicación que se usa cuando el puntero del mouse se mueve dentro de la parte de la ventana del modo lector que se ha declarado como el área de desplazamiento activa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll (función de devolución de llamada) controles de Windows
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996329"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="c16ad-104">Función de devolución de llamada ReaderScroll</span><span class="sxs-lookup"><span data-stu-id="c16ad-104">ReaderScroll callback function</span></span>

<span data-ttu-id="c16ad-105">\[*ReaderScroll* está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="c16ad-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c16ad-106">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c16ad-107">Función de devolución de llamada definida por la aplicación que se usa cuando el puntero del mouse se mueve dentro de la parte de la ventana del modo lector que se ha declarado como el área de desplazamiento activa.</span><span class="sxs-lookup"><span data-stu-id="c16ad-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16ad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c16ad-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="c16ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c16ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c16ad-110">*PRMI* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16ad-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="c16ad-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="c16ad-112">Puntero a la estructura [**READERMODEINFO**](readermodeinfo.md) que se pasó a la función [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="c16ad-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="c16ad-113">Esta estructura define la ventana de modo lector y el área de desplazamiento activa.</span><span class="sxs-lookup"><span data-stu-id="c16ad-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="c16ad-114">*DX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16ad-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c16ad-115">Type: **int**</span></span>

<span data-ttu-id="c16ad-116">Distancia que se va a desplazar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c16ad-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="c16ad-117">Si \_ se establece la marca RMF VERTICALONLY en la estructura [**READERMODEINFO**](readermodeinfo.md) , este valor siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="c16ad-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="c16ad-118">*DY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16ad-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c16ad-119">Type: **int**</span></span>

<span data-ttu-id="c16ad-120">Distancia que se va a desplazar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c16ad-120">The distance to scroll vertically.</span></span> <span data-ttu-id="c16ad-121">Si \_ se establece la marca RMF HORIZONTALONLY en la estructura [**READERMODEINFO**](readermodeinfo.md) , este valor siempre es 0.</span><span class="sxs-lookup"><span data-stu-id="c16ad-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c16ad-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c16ad-122">Return value</span></span>

<span data-ttu-id="c16ad-123">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c16ad-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c16ad-124">Esta función siempre debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="c16ad-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c16ad-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c16ad-125">Remarks</span></span>

<span data-ttu-id="c16ad-126">Cuando la aplicación recibe la notificación de esta función, la aplicación es responsable de desplazar la ventana del modo lector en la dirección especificada por los parámetros *DX* y *DY* .</span><span class="sxs-lookup"><span data-stu-id="c16ad-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c16ad-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c16ad-127">Examples</span></span>

<span data-ttu-id="c16ad-128">En el ejemplo siguiente se describe una implementación de esta función con una función personalizada para realizar el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c16ad-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="c16ad-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c16ad-129">Requirements</span></span>



| <span data-ttu-id="c16ad-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c16ad-130">Requirement</span></span> | <span data-ttu-id="c16ad-131">Value</span><span class="sxs-lookup"><span data-stu-id="c16ad-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c16ad-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c16ad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c16ad-133">Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c16ad-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c16ad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c16ad-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c16ad-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

