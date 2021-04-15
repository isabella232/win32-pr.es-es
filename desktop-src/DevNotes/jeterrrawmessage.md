---
description: Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error de jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649519"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="77ec3-103">JetErrRawMessage función)</span><span class="sxs-lookup"><span data-stu-id="77ec3-103">JetErrRawMessage function</span></span>

<span data-ttu-id="77ec3-104">Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error de jet.</span><span class="sxs-lookup"><span data-stu-id="77ec3-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ec3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77ec3-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="77ec3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77ec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ec3-107">*ERR*</span><span class="sxs-lookup"><span data-stu-id="77ec3-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-108">Error de jet que corresponde a la información que se obtiene.</span><span class="sxs-lookup"><span data-stu-id="77ec3-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-109">*pIda*</span><span class="sxs-lookup"><span data-stu-id="77ec3-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-110">Puntero a IDA.</span><span class="sxs-lookup"><span data-stu-id="77ec3-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="77ec3-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-112">Puntero al mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="77ec3-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-113">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="77ec3-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-114">Recuento del número de bytes del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="77ec3-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="77ec3-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-116">Puntero al número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="77ec3-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-117">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="77ec3-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-118">Puntero al identificador de contexto que está asociado con el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="77ec3-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="77ec3-119">*pwszHelp/archivo*</span><span class="sxs-lookup"><span data-stu-id="77ec3-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="77ec3-120">Apunta a un puntero al archivo que explica el error.</span><span class="sxs-lookup"><span data-stu-id="77ec3-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ec3-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77ec3-121">Return value</span></span>

<span data-ttu-id="77ec3-122">Si la función se ejecuta correctamente, devuelve **jet \_ errSuccess**; de lo contrario, devuelve un mensaje de error sin formato que indica el motivo específico del error.</span><span class="sxs-lookup"><span data-stu-id="77ec3-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="77ec3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77ec3-123">Remarks</span></span>

<span data-ttu-id="77ec3-124">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="77ec3-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ec3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ec3-125">Requirements</span></span>



| <span data-ttu-id="77ec3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ec3-126">Requirement</span></span> | <span data-ttu-id="77ec3-127">Value</span><span class="sxs-lookup"><span data-stu-id="77ec3-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77ec3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77ec3-128">DLL</span></span><br/> | <dl> <span data-ttu-id="77ec3-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77ec3-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
