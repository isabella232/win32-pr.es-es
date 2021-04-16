---
description: Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace función)
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649673"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="b9d2b-103">AsyncStringTrace función)</span><span class="sxs-lookup"><span data-stu-id="b9d2b-103">AsyncStringTrace function</span></span>

<span data-ttu-id="b9d2b-104">Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="b9d2b-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9d2b-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="b9d2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9d2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d2b-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9d2b-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d2b-108">Parámetro de seguimiento de 32 bits que se usa para el filtrado en el nivel de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b9d2b-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="b9d2b-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="b9d2b-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d2b-110">Cadena terminada en cero que describe el formato del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b9d2b-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="b9d2b-111">*dor*</span><span class="sxs-lookup"><span data-stu-id="b9d2b-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d2b-112">Un marcador para las funciones de **vsprintf** .</span><span class="sxs-lookup"><span data-stu-id="b9d2b-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d2b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9d2b-113">Return value</span></span>

<span data-ttu-id="b9d2b-114">Esta función devuelve la longitud de la instrucción de seguimiento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b9d2b-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d2b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9d2b-115">Remarks</span></span>

<span data-ttu-id="b9d2b-116">Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el protocolo de transferencia de noticias en red (NNTP).</span><span class="sxs-lookup"><span data-stu-id="b9d2b-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="b9d2b-117">El tipo de datos de la **\_ lista va** es un tipo estándar que se usa para almacenar la información necesaria para las macros de fin **\_ arg** y **\_ fin** .</span><span class="sxs-lookup"><span data-stu-id="b9d2b-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="b9d2b-118">Para obtener más información, consulte [tipos estándar](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="b9d2b-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="b9d2b-119">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b9d2b-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d2b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9d2b-120">Requirements</span></span>



| <span data-ttu-id="b9d2b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d2b-121">Requirement</span></span> | <span data-ttu-id="b9d2b-122">Value</span><span class="sxs-lookup"><span data-stu-id="b9d2b-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d2b-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9d2b-123">DLL</span></span><br/> | <dl> <span data-ttu-id="b9d2b-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9d2b-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

