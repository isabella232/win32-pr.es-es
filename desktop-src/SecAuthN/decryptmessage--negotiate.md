---
description: Descifra un mensaje mediante Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (Negotiate) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720386"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="1ffa8-103">DecryptMessage (Negotiate) (función)</span><span class="sxs-lookup"><span data-stu-id="1ffa8-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="1ffa8-104">La función **DecryptMessage (Negotiate)** descifra un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="1ffa8-105">Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="1ffa8-106">Se puede llamar a [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) y **DecryptMessage (Negotiate)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="1ffa8-107">Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffa8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ffa8-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="1ffa8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ffa8-109">Parameters</span></span>

<span data-ttu-id="1ffa8-110">*phContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-110">*phContext* \[in\]</span></span>

<span data-ttu-id="1ffa8-111">Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para descifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="1ffa8-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="1ffa8-113">Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="1ffa8-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="1ffa8-114">En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="1ffa8-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="1ffa8-115">Al menos uno de estos datos debe ser de tipo SECBUFFER \_ Data.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="1ffa8-116">Ese búfer contiene el mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="1ffa8-117">El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="1ffa8-118">*MessageSeqNo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="1ffa8-119">El número de secuencia esperado por la aplicación de transporte, si existe.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="1ffa8-120">Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="1ffa8-121">*pfQOP* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="1ffa8-122">Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="1ffa8-123">Este parámetro puede ser la marca siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="1ffa8-124">Value</span><span class="sxs-lookup"><span data-stu-id="1ffa8-124">Value</span></span></th><th><span data-ttu-id="1ffa8-125">Significado</span><span class="sxs-lookup"><span data-stu-id="1ffa8-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="1ffa8-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ffa8-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="1ffa8-127">No se cifró el mensaje, pero se produjo un encabezado o un finalizador.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="1ffa8-128">KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="1ffa8-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ffa8-129">Return value</span></span>

<span data-ttu-id="1ffa8-130">Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1ffa8-131">Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="1ffa8-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ffa8-132">Return code</span></span>                     | <span data-ttu-id="1ffa8-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ffa8-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffa8-134">**s \_ E \_ mensaje incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="1ffa8-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="1ffa8-135">Los datos del búfer de entrada están incompletos.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="1ffa8-136">La aplicación necesita leer más datos del servidor y llamar a [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="1ffa8-137">**s \_ E \_ fuera \_ de \_ secuencia**</span><span class="sxs-lookup"><span data-stu-id="1ffa8-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="1ffa8-138">No se recibió el mensaje en la secuencia correcta.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="1ffa8-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ffa8-139">Remarks</span></span>

<span data-ttu-id="1ffa8-140">A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Negotiate)** y detectará que **DecryptMessage (Negotiate)** se ejecutó correctamente, pero los búferes de salida están vacíos.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="1ffa8-141">Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="1ffa8-142">**Windows XP:** Esta función también se conocía como **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="1ffa8-143">Las aplicaciones ahora deben usar **DecryptMessage (Negotiate)** solamente.</span><span class="sxs-lookup"><span data-stu-id="1ffa8-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ffa8-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ffa8-144">Requirements</span></span>

| <span data-ttu-id="1ffa8-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ffa8-145">Requirement</span></span> | <span data-ttu-id="1ffa8-146">Value</span><span class="sxs-lookup"><span data-stu-id="1ffa8-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1ffa8-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ffa8-147">Minimum supported client</span></span> | <span data-ttu-id="1ffa8-148">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="1ffa8-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ffa8-149">Minimum supported server</span></span> | <span data-ttu-id="1ffa8-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ffa8-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="1ffa8-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ffa8-151">Header</span></span>                   | <span data-ttu-id="1ffa8-152">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="1ffa8-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="1ffa8-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ffa8-153">Library</span></span>                  | <span data-ttu-id="1ffa8-154">SECUR32. lib</span><span class="sxs-lookup"><span data-stu-id="1ffa8-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="1ffa8-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ffa8-155">DLL</span></span>                      | <span data-ttu-id="1ffa8-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="1ffa8-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="1ffa8-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ffa8-157">See also</span></span>

- [<span data-ttu-id="1ffa8-158">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="1ffa8-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="1ffa8-159">**EncryptMessage (Negotiate)**</span><span class="sxs-lookup"><span data-stu-id="1ffa8-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="1ffa8-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="1ffa8-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="1ffa8-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="1ffa8-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
