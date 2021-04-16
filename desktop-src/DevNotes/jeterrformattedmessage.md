---
description: Recupera un identificador de código de error (IDA) y crea la cadena de presentación final cuando se proporciona un error de jet e información de error extendida.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649511"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="98241-103">JetErrFormattedMessage función)</span><span class="sxs-lookup"><span data-stu-id="98241-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="98241-104">Recupera un identificador de código de error (IDA) y crea la cadena de presentación final cuando se proporciona un error de jet e información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="98241-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="98241-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98241-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="98241-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98241-107">*ERR*</span><span class="sxs-lookup"><span data-stu-id="98241-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-108">El número de error de jet que se usa para buscar y dar formato al mensaje de error que se pueda mostrar.</span><span class="sxs-lookup"><span data-stu-id="98241-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="98241-109">*pExtendedErrorInfo*</span><span class="sxs-lookup"><span data-stu-id="98241-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-110">Toda la información de error de jet, incluido el nombre de la base de datos, el nombre de la tabla y cualquier información de error menor.</span><span class="sxs-lookup"><span data-stu-id="98241-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="98241-111">*pIda*</span><span class="sxs-lookup"><span data-stu-id="98241-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-112">Puntero a IDA asociado al código de error específico.</span><span class="sxs-lookup"><span data-stu-id="98241-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="98241-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="98241-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-114">Puntero al mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="98241-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="98241-115">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="98241-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-116">Recuento del número de bytes del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="98241-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="98241-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="98241-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-118">Puntero al número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="98241-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="98241-119">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="98241-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-120">Puntero al identificador de contexto que está asociado con el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="98241-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="98241-121">*pwszHelp/archivo*</span><span class="sxs-lookup"><span data-stu-id="98241-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="98241-122">Un puntero a un puntero al archivo que explica el error.</span><span class="sxs-lookup"><span data-stu-id="98241-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98241-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98241-123">Return value</span></span>

<span data-ttu-id="98241-124">Si la función se ejecuta correctamente, devuelve **jet \_ errSuccess**; de lo contrario, devuelve un mensaje de error con formato que indica el motivo específico del error.</span><span class="sxs-lookup"><span data-stu-id="98241-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="98241-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98241-125">Remarks</span></span>

<span data-ttu-id="98241-126">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="98241-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="98241-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98241-127">Requirements</span></span>



| <span data-ttu-id="98241-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="98241-128">Requirement</span></span> | <span data-ttu-id="98241-129">Value</span><span class="sxs-lookup"><span data-stu-id="98241-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98241-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98241-130">DLL</span></span><br/> | <dl> <span data-ttu-id="98241-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98241-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
