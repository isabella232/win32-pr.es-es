---
description: Libera un objeto de clave, hash o proveedor.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Función SslFreeObject (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908826"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="7d551-103">SslFreeObject función)</span><span class="sxs-lookup"><span data-stu-id="7d551-103">SslFreeObject function</span></span>

<span data-ttu-id="7d551-104">La función **SslFreeObject** libera un objeto Key, hash o Provider.</span><span class="sxs-lookup"><span data-stu-id="7d551-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d551-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d551-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7d551-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d551-107">*hObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d551-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d551-108">Identificador del objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="7d551-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="7d551-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d551-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d551-110">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7d551-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d551-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d551-111">Return value</span></span>

<span data-ttu-id="7d551-112">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="7d551-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7d551-113">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="7d551-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7d551-114">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d551-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7d551-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d551-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7d551-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d551-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7d551-117"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="7d551-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="7d551-118">Un identificador interno no es válido.</span><span class="sxs-lookup"><span data-stu-id="7d551-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="7d551-119"><dt>**Estado \_ de \_Identificador no válido**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="7d551-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="7d551-120">El identificador proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="7d551-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7d551-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d551-121">Requirements</span></span>



| <span data-ttu-id="7d551-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d551-122">Requirement</span></span> | <span data-ttu-id="7d551-123">Value</span><span class="sxs-lookup"><span data-stu-id="7d551-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d551-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d551-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d551-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7d551-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d551-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d551-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d551-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d551-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d551-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d551-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d551-129"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d551-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7d551-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d551-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d551-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d551-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




