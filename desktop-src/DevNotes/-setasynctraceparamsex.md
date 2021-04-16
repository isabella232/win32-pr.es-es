---
description: Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649683"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="153ae-103">SetAsyncTraceParamsEx función)</span><span class="sxs-lookup"><span data-stu-id="153ae-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="153ae-104">Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="153ae-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="153ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="153ae-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="153ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="153ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153ae-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="153ae-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="153ae-108">Nombre del módulo que está asociado con el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="153ae-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="153ae-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="153ae-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="153ae-110">Nombre del archivo de código fuente que contiene la excepción.</span><span class="sxs-lookup"><span data-stu-id="153ae-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="153ae-111">*Tarea*</span><span class="sxs-lookup"><span data-stu-id="153ae-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="153ae-112">Número de línea de la excepción en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="153ae-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="153ae-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="153ae-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="153ae-114">Nombre de la función de la excepción.</span><span class="sxs-lookup"><span data-stu-id="153ae-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="153ae-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="153ae-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="153ae-116">Una constante de marca de seguimiento que representa uno de los tipos de seguimiento disponibles.</span><span class="sxs-lookup"><span data-stu-id="153ae-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="153ae-117">Este parámetro puede ser cualquiera de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="153ae-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="153ae-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Irrecuperable \_ \_Máscara de seguimiento** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="153ae-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Error \_ de \_Máscara de seguimiento** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="153ae-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Depuración \_ \_Máscara de seguimiento** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="153ae-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Estado \_ de \_Máscara de seguimiento** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="153ae-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Inactivo \_ \_Máscara de seguimiento** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="153ae-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Mensaje \_ de \_Máscara de seguimiento** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="153ae-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="153ae-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Todo \_ \_Máscara de seguimiento** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="153ae-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153ae-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="153ae-125">Return value</span></span>

<span data-ttu-id="153ae-126">Esta función devuelve 1 si la función se ejecuta correctamente; de lo contrario, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="153ae-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="153ae-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="153ae-127">Remarks</span></span>

<span data-ttu-id="153ae-128">Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el protocolo de transferencia de noticias en red (NNTP).</span><span class="sxs-lookup"><span data-stu-id="153ae-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="153ae-129">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="153ae-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="153ae-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="153ae-130">Requirements</span></span>



| <span data-ttu-id="153ae-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="153ae-131">Requirement</span></span> | <span data-ttu-id="153ae-132">Value</span><span class="sxs-lookup"><span data-stu-id="153ae-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="153ae-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="153ae-133">DLL</span></span><br/> | <dl> <span data-ttu-id="153ae-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153ae-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
