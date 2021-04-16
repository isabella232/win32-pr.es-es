---
description: Recupera una cadena de mensaje sin formato cuando se proporciona un identificador de código de error (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671544"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="02ce7-103">JetErrIDARawMessage función)</span><span class="sxs-lookup"><span data-stu-id="02ce7-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="02ce7-104">Recupera una cadena de mensaje sin formato cuando se proporciona un identificador de código de error (IDA).</span><span class="sxs-lookup"><span data-stu-id="02ce7-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ce7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02ce7-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="02ce7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02ce7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ce7-107">*Ida*</span><span class="sxs-lookup"><span data-stu-id="02ce7-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-108">Número que se asigna a un código de error específico y se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="02ce7-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="02ce7-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="02ce7-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-110">Puntero al mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="02ce7-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="02ce7-111">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="02ce7-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-112">Recuento del número de bytes del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="02ce7-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="02ce7-113">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="02ce7-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-114">Puntero al número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="02ce7-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="02ce7-115">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="02ce7-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-116">Puntero al identificador de contexto que está asociado con el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="02ce7-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="02ce7-117">*pwszHelp/archivo*</span><span class="sxs-lookup"><span data-stu-id="02ce7-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="02ce7-118">Un puntero a un puntero al archivo que explica el error.</span><span class="sxs-lookup"><span data-stu-id="02ce7-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ce7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02ce7-119">Return value</span></span>

<span data-ttu-id="02ce7-120">Si la función se ejecuta correctamente, devuelve **jet \_ errSuccess**; de lo contrario, devuelve un mensaje sin formato que indica el motivo específico del error.</span><span class="sxs-lookup"><span data-stu-id="02ce7-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="02ce7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02ce7-121">Remarks</span></span>

<span data-ttu-id="02ce7-122">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="02ce7-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ce7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02ce7-123">Requirements</span></span>



| <span data-ttu-id="02ce7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ce7-124">Requirement</span></span> | <span data-ttu-id="02ce7-125">Value</span><span class="sxs-lookup"><span data-stu-id="02ce7-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02ce7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02ce7-126">DLL</span></span><br/> | <dl> <span data-ttu-id="02ce7-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02ce7-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
