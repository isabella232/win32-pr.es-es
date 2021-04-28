---
description: 'Función SetAsyncTraceParamsEx: finaliza la configuración de un búfer de seguimiento con campos opcionales para seguimientos de estilo sprintf.'
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Función SetAsyncTraceParamsEx
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
ms.openlocfilehash: 5a9dc0eee2f4ea3f65fa45914c3340a99ac2d45b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085773"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="9f5e5-103">Función SetAsyncTraceParamsEx</span><span class="sxs-lookup"><span data-stu-id="9f5e5-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="9f5e5-104">Finaliza la configuración de un búfer de seguimiento con campos opcionales para **seguimientos sprintf-style.**</span><span class="sxs-lookup"><span data-stu-id="9f5e5-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f5e5-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="9f5e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f5e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5e5-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5e5-108">Nombre del módulo asociado al seguimiento.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="9f5e5-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5e5-110">Nombre del archivo de origen que contiene la excepción.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="9f5e5-111">*lLine*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5e5-112">Número de línea de la excepción en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="9f5e5-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5e5-114">Nombre de función de la excepción.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="9f5e5-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="9f5e5-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5e5-116">Constante de marca de seguimiento que representa uno de los tipos de seguimiento disponibles.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="9f5e5-117">Este parámetro puede ser cualquiera de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9f5e5-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL \_ TRACE \_ MASK** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR \_ TRACE \_ MASK** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG \_ TRACE \_ MASK** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE \_ TRACE \_ MASK** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ TRACE \_ MASK** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE \_ TRACE \_ MASK** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="9f5e5-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL \_ TRACE \_ MASK** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f5e5-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f5e5-125">Return value</span></span>

<span data-ttu-id="9f5e5-126">Esta función devuelve 1 si la función se realiza correctamente; de lo contrario, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="9f5e5-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5e5-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f5e5-127">Remarks</span></span>

<span data-ttu-id="9f5e5-128">Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el Protocolo de transferencia de noticias de red (NNTP).</span><span class="sxs-lookup"><span data-stu-id="9f5e5-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="9f5e5-129">Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="9f5e5-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f5e5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f5e5-130">Requirements</span></span>



| <span data-ttu-id="9f5e5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f5e5-131">Requirement</span></span> | <span data-ttu-id="9f5e5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="9f5e5-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5e5-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f5e5-133">DLL</span></span><br/> | <dl> <span data-ttu-id="9f5e5-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f5e5-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
