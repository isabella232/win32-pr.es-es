---
description: Establece la seguridad de una clave del registro abierta en un subárbol del registro sin conexión.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Función ORSetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670379"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="78868-103">ORSetKeySecurity función)</span><span class="sxs-lookup"><span data-stu-id="78868-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="78868-104">Establece la seguridad de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="78868-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="78868-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78868-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="78868-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78868-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78868-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78868-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="78868-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="78868-109">*SecurityInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="78868-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78868-110">Marcas de bits que indican el tipo de información de seguridad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="78868-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="78868-111">Este parámetro puede ser una combinación de las marcas de bits de [ \_ información de seguridad](../secauthz/security-information.md) .</span><span class="sxs-lookup"><span data-stu-id="78868-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="78868-112">*pSecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="78868-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78868-113">Puntero a una estructura [de \_ descriptores de seguridad](/windows/win32/api/winnt/ns-winnt-security_descriptor) que especifica los atributos de seguridad que se van a establecer para la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="78868-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78868-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78868-114">Return value</span></span>

<span data-ttu-id="78868-115">Si la función se ejecuta correctamente, la función devuelve el ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="78868-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="78868-116">Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="78868-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="78868-117">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="78868-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="78868-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78868-118">Requirements</span></span>



| <span data-ttu-id="78868-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78868-119">Requirement</span></span> | <span data-ttu-id="78868-120">Value</span><span class="sxs-lookup"><span data-stu-id="78868-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78868-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="78868-121">Redistributable</span></span><br/> | <span data-ttu-id="78868-122">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="78868-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="78868-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78868-123">Header</span></span><br/>          | <dl> <span data-ttu-id="78868-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="78868-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="78868-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78868-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="78868-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78868-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78868-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="78868-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78868-128">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="78868-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="78868-129">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="78868-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="78868-130">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="78868-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="78868-131">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="78868-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="78868-132">descriptor de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="78868-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="78868-133">información de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="78868-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
