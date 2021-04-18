---
description: Recupera una copia del descriptor de seguridad que protege la clave del registro abierta especificada en un subárbol del registro sin conexión.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Función ORGetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649981"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="2cc32-103">ORGetKeySecurity función)</span><span class="sxs-lookup"><span data-stu-id="2cc32-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="2cc32-104">Recupera una copia del descriptor de seguridad que protege la clave del registro abierta especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2cc32-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cc32-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="2cc32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cc32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc32-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2cc32-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc32-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2cc32-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2cc32-109">*SecurityInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2cc32-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc32-110">Valor [de \_ información de seguridad](../secauthz/security-information.md) que indica la información de seguridad solicitada.</span><span class="sxs-lookup"><span data-stu-id="2cc32-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="2cc32-111">*pSecurityDescriptor* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2cc32-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc32-112">Un puntero a un búfer que recibe una copia del descriptor de seguridad solicitado.</span><span class="sxs-lookup"><span data-stu-id="2cc32-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="2cc32-113">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2cc32-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2cc32-114">*lpcbSecurityDescriptor* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2cc32-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc32-115">Puntero a una variable que especifica el tamaño, en bytes, del búfer al que apunta el parámetro *pSecurityDescriptor* .</span><span class="sxs-lookup"><span data-stu-id="2cc32-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="2cc32-116">Cuando la función devuelve, la variable contiene el número de bytes escritos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="2cc32-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc32-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cc32-117">Return value</span></span>

<span data-ttu-id="2cc32-118">Si la función se ejecuta correctamente, la función devuelve el ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2cc32-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2cc32-119">Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="2cc32-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="2cc32-120">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="2cc32-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="2cc32-121">Si el búfer especificado por el parámetro *pSecurityDescriptor* es demasiado pequeño, la función devuelve un error de \_ búfer insuficiente \_ y el parámetro *lpcbSecurityDescriptor* contiene el número de bytes necesarios para el descriptor de seguridad solicitado.</span><span class="sxs-lookup"><span data-stu-id="2cc32-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc32-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc32-122">Requirements</span></span>



| <span data-ttu-id="2cc32-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc32-123">Requirement</span></span> | <span data-ttu-id="2cc32-124">Value</span><span class="sxs-lookup"><span data-stu-id="2cc32-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc32-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2cc32-125">Redistributable</span></span><br/> | <span data-ttu-id="2cc32-126">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2cc32-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="2cc32-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cc32-127">Header</span></span><br/>          | <dl> <span data-ttu-id="2cc32-128"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc32-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cc32-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cc32-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="2cc32-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cc32-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc32-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cc32-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc32-132">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="2cc32-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="2cc32-133">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="2cc32-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="2cc32-134">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="2cc32-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="2cc32-135">información de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="2cc32-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
