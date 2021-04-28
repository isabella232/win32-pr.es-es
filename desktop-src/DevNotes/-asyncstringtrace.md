---
description: 'Función AsyncStringTrace: finaliza la configuración de un búfer de seguimiento con campos opcionales para seguimientos de estilo sprintf.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Función AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085803"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="d1932-103">Función AsyncStringTrace</span><span class="sxs-lookup"><span data-stu-id="d1932-103">AsyncStringTrace function</span></span>

<span data-ttu-id="d1932-104">Finaliza la configuración de un búfer de seguimiento con campos opcionales para **seguimientos sprintf-style.**</span><span class="sxs-lookup"><span data-stu-id="d1932-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1932-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1932-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="d1932-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1932-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1932-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1932-108">Parámetro de seguimiento de 32 bits que se usa para el filtrado en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d1932-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="d1932-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="d1932-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d1932-110">Cadena terminada en cero que describe el formato del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d1932-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="d1932-111">*Marcador*</span><span class="sxs-lookup"><span data-stu-id="d1932-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="d1932-112">Marcador para las **funciones vsprintf.**</span><span class="sxs-lookup"><span data-stu-id="d1932-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1932-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1932-113">Return value</span></span>

<span data-ttu-id="d1932-114">Esta función devuelve la longitud de la instrucción de seguimiento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d1932-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1932-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1932-115">Remarks</span></span>

<span data-ttu-id="d1932-116">Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el Protocolo de transferencia de noticias de red (NNTP).</span><span class="sxs-lookup"><span data-stu-id="d1932-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="d1932-117">El **tipo de datos va \_ list** es un tipo estándar que se usa para contener la información necesaria para **las macros va \_ arg** **y va \_ end.**</span><span class="sxs-lookup"><span data-stu-id="d1932-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="d1932-118">Para obtener más información, vea [Tipos estándar.](/cpp/c-runtime-library/standard-types?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="d1932-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="d1932-119">Esta función no tiene ningún archivo de encabezado o biblioteca de importación asociado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="d1932-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1932-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1932-120">Requirements</span></span>



| <span data-ttu-id="d1932-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1932-121">Requirement</span></span> | <span data-ttu-id="d1932-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d1932-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1932-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1932-123">DLL</span></span><br/> | <dl> <span data-ttu-id="d1932-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1932-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

