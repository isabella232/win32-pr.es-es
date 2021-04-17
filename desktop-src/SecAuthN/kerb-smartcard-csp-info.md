---
description: Contiene información acerca de un proveedor de servicios criptográficos (CSP) de tarjetas inteligentes.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Estructura de KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652728"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="07568-103">\_Estructura de \_ información de CSP de tarjeta inteligente Kerb \_</span><span class="sxs-lookup"><span data-stu-id="07568-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="07568-104">La estructura de **\_ \_ \_ información de CSP** de tarjeta inteligente Kerb contiene información sobre un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="07568-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="07568-105">Esta estructura no se declara en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="07568-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="07568-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07568-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="07568-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="07568-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07568-108">**dwCspInfoLen**</span><span class="sxs-lookup"><span data-stu-id="07568-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="07568-109">Tamaño, en bytes, de esta estructura, incluidos los datos anexados.</span><span class="sxs-lookup"><span data-stu-id="07568-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="07568-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="07568-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="07568-111">El tipo de mensaje que se pasa.</span><span class="sxs-lookup"><span data-stu-id="07568-111">The type of message being passed.</span></span> <span data-ttu-id="07568-112">Este miembro debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="07568-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="07568-113">**ContextInformation**</span><span class="sxs-lookup"><span data-stu-id="07568-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="07568-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07568-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="07568-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="07568-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="07568-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07568-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="07568-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="07568-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="07568-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07568-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="07568-119">**Especificación**</span><span class="sxs-lookup"><span data-stu-id="07568-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="07568-120">Clave privada que se utilizará en el contenedor de claves especificado en el búfer **bBuffer**.</span><span class="sxs-lookup"><span data-stu-id="07568-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="07568-121">La clave puede ser uno de los siguientes valores, definidos en WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="07568-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="07568-122">Value</span><span class="sxs-lookup"><span data-stu-id="07568-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="07568-123">Significado</span><span class="sxs-lookup"><span data-stu-id="07568-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="07568-124"><dt>**En \_ KEYEXCHANGE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="07568-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="07568-125">La clave es una clave de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="07568-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="07568-126"><dt>**En \_ FIRMA**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="07568-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="07568-127">La clave es una clave de firma.</span><span class="sxs-lookup"><span data-stu-id="07568-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="07568-128">**nCardNameOffset**</span><span class="sxs-lookup"><span data-stu-id="07568-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="07568-129">Número de caracteres del búfer **bBuffer** que preceden al nombre de la tarjeta inteligente en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="07568-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07568-130">Si no se proporciona el nombre de la tarjeta inteligente, el búfer debe contener una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="07568-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="07568-131">**nReaderNameOffset**</span><span class="sxs-lookup"><span data-stu-id="07568-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="07568-132">Número de caracteres del búfer **bBuffer** que preceden al nombre del lector de tarjetas inteligentes en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="07568-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07568-133">Si no se proporciona el nombre del lector de tarjeta inteligente, el búfer debe contener una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="07568-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="07568-134">**nContainerNameOffset**</span><span class="sxs-lookup"><span data-stu-id="07568-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="07568-135">Número de caracteres del búfer **bBuffer** que preceden al nombre del contenedor de claves en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="07568-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="07568-136">Esta cadena no puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="07568-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="07568-137">**nCSPNameOffset**</span><span class="sxs-lookup"><span data-stu-id="07568-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="07568-138">Número de caracteres del búfer **bBuffer** que preceden al nombre del CSP en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="07568-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="07568-139">**bBuffer**</span><span class="sxs-lookup"><span data-stu-id="07568-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="07568-140">Matriz de caracteres inicializada en una longitud de `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="07568-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="07568-141">Este búfer contiene los nombres a los que hacen referencia los miembros **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** y **nCSPNameOffset** , así como los datos adicionales proporcionados por el CSP.</span><span class="sxs-lookup"><span data-stu-id="07568-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="07568-142">Los nombres que no se proporcionen deben representarse en este búfer mediante cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="07568-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07568-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07568-143">Remarks</span></span>

<span data-ttu-id="07568-144">Cuando se serializa esta estructura, los miembros de la estructura se deben alinear con los límites que son múltiplos de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="07568-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="07568-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07568-145">Requirements</span></span>



| <span data-ttu-id="07568-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="07568-146">Requirement</span></span> | <span data-ttu-id="07568-147">Value</span><span class="sxs-lookup"><span data-stu-id="07568-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07568-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07568-148">Minimum supported client</span></span><br/> | <span data-ttu-id="07568-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="07568-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07568-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07568-150">Minimum supported server</span></span><br/> | <span data-ttu-id="07568-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="07568-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07568-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="07568-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07568-153">**Inicio de sesión de \_ certificado Kerb \_**</span><span class="sxs-lookup"><span data-stu-id="07568-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
