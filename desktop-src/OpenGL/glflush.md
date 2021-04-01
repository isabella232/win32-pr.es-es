---
title: función glFlush (GL. h)
description: La función glFlush fuerza la ejecución de funciones OpenGL en tiempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush (función) OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804057"
---
# <a name="glflush-function"></a><span data-ttu-id="8c81f-104">glFlush función)</span><span class="sxs-lookup"><span data-stu-id="8c81f-104">glFlush function</span></span>

<span data-ttu-id="8c81f-105">La función **glFlush** fuerza la ejecución de funciones OpenGL en tiempo finito.</span><span class="sxs-lookup"><span data-stu-id="8c81f-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c81f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c81f-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="8c81f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c81f-107">Parameters</span></span>

<span data-ttu-id="8c81f-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c81f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c81f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c81f-109">Return value</span></span>

<span data-ttu-id="8c81f-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c81f-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8c81f-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8c81f-111">Error codes</span></span>

<span data-ttu-id="8c81f-112">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="8c81f-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8c81f-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c81f-113">Name</span></span>                                                                                                  | <span data-ttu-id="8c81f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8c81f-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c81f-115"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c81f-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8c81f-116">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8c81f-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8c81f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c81f-117">Remarks</span></span>

<span data-ttu-id="8c81f-118">Distintos comandos de búfer de implementación de OpenGL en varias ubicaciones diferentes, incluidos los búferes de red y el propio acelerador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="8c81f-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="8c81f-119">La función **glFlush** vacía todos estos búferes, lo que hace que todos los comandos emitidos se ejecuten tan pronto como los acepte el motor de representación real.</span><span class="sxs-lookup"><span data-stu-id="8c81f-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="8c81f-120">Aunque es posible que esta ejecución no se complete en un período de tiempo determinado, se completa en un intervalo de tiempo finito.</span><span class="sxs-lookup"><span data-stu-id="8c81f-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="8c81f-121">Dado que cualquier programa de OpenGL puede ejecutarse a través de una red o en un acelerador que almacene en búfer comandos, asegúrese de llamar a **glFlush** en cualquier programa que requiera que se hayan completado todos los comandos previamente emitidos.</span><span class="sxs-lookup"><span data-stu-id="8c81f-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="8c81f-122">Por ejemplo, llame a **glFlush** antes de esperar la entrada del usuario que depende de la imagen generada.</span><span class="sxs-lookup"><span data-stu-id="8c81f-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="8c81f-123">La función **glFlush** puede devolver en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="8c81f-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="8c81f-124">No espera hasta que se complete la ejecución de todas las funciones OpenGL emitidas previamente.</span><span class="sxs-lookup"><span data-stu-id="8c81f-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c81f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c81f-125">Requirements</span></span>



| <span data-ttu-id="8c81f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c81f-126">Requirement</span></span> | <span data-ttu-id="8c81f-127">Value</span><span class="sxs-lookup"><span data-stu-id="8c81f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c81f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c81f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8c81f-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c81f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8c81f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c81f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8c81f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c81f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c81f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c81f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c81f-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c81f-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8c81f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c81f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c81f-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c81f-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c81f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c81f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c81f-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c81f-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c81f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c81f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c81f-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8c81f-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8c81f-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8c81f-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8c81f-141">**glFinish**</span><span class="sxs-lookup"><span data-stu-id="8c81f-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





