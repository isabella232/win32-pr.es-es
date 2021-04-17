---
title: Mensaje de TB_ADDSTRING (commctrl. h)
description: Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658407"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="368ef-104">Message TB de \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="368ef-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="368ef-105">Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="368ef-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="368ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="368ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="368ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="368ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="368ef-108">Identificador de la instancia de módulo con un archivo ejecutable que contiene el recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="368ef-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="368ef-109">Si *lParam* en su lugar apunta a una matriz de caracteres con una o más cadenas, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="368ef-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="368ef-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="368ef-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="368ef-111">Identificador de recurso para el recurso de cadena o un puntero a una matriz TCHAR.</span><span class="sxs-lookup"><span data-stu-id="368ef-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="368ef-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="368ef-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="368ef-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="368ef-113">Return value</span></span>

<span data-ttu-id="368ef-114">Devuelve el índice de la primera cadena nueva si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="368ef-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="368ef-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="368ef-115">Remarks</span></span>

<span data-ttu-id="368ef-116">Si *wParam* es **null**, *lParam* apunta a una matriz de caracteres con una o más cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="368ef-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="368ef-117">La última cadena de la matriz debe terminar con dos caracteres null.</span><span class="sxs-lookup"><span data-stu-id="368ef-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="368ef-118">Si *wParam* es el hInstance de la aplicación o de otro módulo que contiene un recurso de cadena, *lParam* es el identificador de recursos de la cadena.</span><span class="sxs-lookup"><span data-stu-id="368ef-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="368ef-119">Cada elemento de la cadena debe comenzar por un carácter separador arbitrario y la cadena debe terminar con dos caracteres tales.</span><span class="sxs-lookup"><span data-stu-id="368ef-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="368ef-120">Por ejemplo, el texto de tres botones podría aparecer en la tabla de cadenas como "/New/Open/Save//".</span><span class="sxs-lookup"><span data-stu-id="368ef-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="368ef-121">El mensaje devuelve el índice de "New" en el grupo de cadenas de la barra de herramientas y los demás elementos están en posiciones consecutivas.</span><span class="sxs-lookup"><span data-stu-id="368ef-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="368ef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="368ef-122">Requirements</span></span>



| <span data-ttu-id="368ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="368ef-123">Requirement</span></span> | <span data-ttu-id="368ef-124">Value</span><span class="sxs-lookup"><span data-stu-id="368ef-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="368ef-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="368ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="368ef-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="368ef-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="368ef-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="368ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="368ef-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="368ef-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="368ef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="368ef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="368ef-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="368ef-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="368ef-131">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="368ef-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="368ef-132">**TB \_ ADDSTRINGW** (Unicode) y **TB \_ ADDSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="368ef-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





