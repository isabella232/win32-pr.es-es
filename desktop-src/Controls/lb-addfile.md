---
title: Mensaje de LB_ADDFILE (Winuser. h)
description: Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492154"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="b0529-104">Mensaje de LB \_ ADDFILE</span><span class="sxs-lookup"><span data-stu-id="b0529-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="b0529-105">Agrega el nombre de archivo especificado a un cuadro de lista que contiene una lista de directorios.</span><span class="sxs-lookup"><span data-stu-id="b0529-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0529-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0529-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0529-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0529-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b0529-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0529-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0529-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0529-110">Un puntero a un búfer que especifica el nombre del archivo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b0529-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0529-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0529-111">Return value</span></span>

<span data-ttu-id="b0529-112">El valor devuelto es el índice de base cero del archivo que se agregó, o LB \_ Err si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b0529-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0529-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0529-113">Remarks</span></span>

<span data-ttu-id="b0529-114">La función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) debe haber rellenado el cuadro de lista al que se agrega *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b0529-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="b0529-115">El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="b0529-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="b0529-116">Reserva la cantidad de memoria especificada para que los mensajes de la **lb \_** de la carga posterior tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="b0529-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="b0529-117">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b0529-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="b0529-118">Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="b0529-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="b0529-119">En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="b0529-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="b0529-120">Esto puede causar problemas.</span><span class="sxs-lookup"><span data-stu-id="b0529-120">This can cause problems.</span></span> <span data-ttu-id="b0529-121">Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán.</span><span class="sxs-lookup"><span data-stu-id="b0529-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="b0529-122">Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="b0529-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0529-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0529-123">Requirements</span></span>



| <span data-ttu-id="b0529-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0529-124">Requirement</span></span> | <span data-ttu-id="b0529-125">Value</span><span class="sxs-lookup"><span data-stu-id="b0529-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0529-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0529-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b0529-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0529-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b0529-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0529-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b0529-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0529-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b0529-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0529-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0529-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0529-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0529-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0529-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0529-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b0529-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0529-134">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="b0529-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="b0529-135">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="b0529-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





