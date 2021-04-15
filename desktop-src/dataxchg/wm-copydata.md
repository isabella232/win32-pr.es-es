---
title: Mensaje de WM_COPYDATA (Winuser. h)
description: Una aplicación envía el mensaje de COPYDATA de WM \_ para pasar datos a otra aplicación.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Intercambio de datos de mensajes de WM_COPYDATA
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491069"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="6f685-104">Mensaje de COPYDATA de WM \_</span><span class="sxs-lookup"><span data-stu-id="6f685-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="6f685-105">Una aplicación envía el mensaje de **\_ COPYDATA de WM** para pasar datos a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f685-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="6f685-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f685-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f685-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f685-108">Identificador de la ventana que pasa los datos.</span><span class="sxs-lookup"><span data-stu-id="6f685-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="6f685-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f685-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f685-110">Puntero a una estructura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contiene los datos que se van a pasar.</span><span class="sxs-lookup"><span data-stu-id="6f685-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f685-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f685-111">Return value</span></span>

<span data-ttu-id="6f685-112">Si la aplicación receptora procesa este mensaje, debe devolver **true**; de lo contrario, debería devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="6f685-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f685-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f685-113">Remarks</span></span>

<span data-ttu-id="6f685-114">Los datos que se pasan no deben contener punteros u otras referencias a objetos a los que no se puede tener acceso a través de la aplicación que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="6f685-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="6f685-115">Mientras se envía este mensaje, otro subproceso del proceso de envío no debe cambiar los datos a los que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="6f685-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="6f685-116">La aplicación receptora debe tener en cuenta los datos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6f685-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="6f685-117">El parámetro *lParam* solo es válido durante el procesamiento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6f685-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="6f685-118">La aplicación receptora no debe liberar la memoria a la que hace referencia *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6f685-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="6f685-119">Si la aplicación receptora debe tener acceso a los datos después de que se devuelva [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , debe copiar los datos en un búfer local.</span><span class="sxs-lookup"><span data-stu-id="6f685-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="6f685-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6f685-120">Examples</span></span>

<span data-ttu-id="6f685-121">Para obtener un ejemplo, vea uso de la [copia de datos](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="6f685-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f685-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f685-122">Requirements</span></span>



| <span data-ttu-id="6f685-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f685-123">Requirement</span></span> | <span data-ttu-id="6f685-124">Value</span><span class="sxs-lookup"><span data-stu-id="6f685-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f685-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f685-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f685-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f685-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f685-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f685-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f685-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f685-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f685-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f685-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f685-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f685-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f685-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f685-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f685-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6f685-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f685-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6f685-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="6f685-134">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="6f685-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

