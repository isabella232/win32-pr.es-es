---
description: Descifra un mensaje mediante Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Función DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154772"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="6f30d-103">Función DecryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="6f30d-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="6f30d-104">La función **DecryptMessage (Kerberos)** descifra un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6f30d-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="6f30d-105">Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.</span><span class="sxs-lookup"><span data-stu-id="6f30d-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="6f30d-106">Se puede llamar a [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) y **DecryptMessage (Kerberos)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando.</span><span class="sxs-lookup"><span data-stu-id="6f30d-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="6f30d-107">Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.</span><span class="sxs-lookup"><span data-stu-id="6f30d-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f30d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f30d-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="6f30d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f30d-109">Parameters</span></span>

<span data-ttu-id="6f30d-110">*phContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-110">*phContext* \[in\]</span></span>

<span data-ttu-id="6f30d-111">Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para descifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6f30d-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="6f30d-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="6f30d-113">Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="6f30d-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="6f30d-114">En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="6f30d-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="6f30d-115">El búfer contiene el mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="6f30d-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="6f30d-116">El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.</span><span class="sxs-lookup"><span data-stu-id="6f30d-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="6f30d-117">*MessageSeqNo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="6f30d-118">El número de secuencia esperado por la aplicación de transporte, si existe.</span><span class="sxs-lookup"><span data-stu-id="6f30d-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="6f30d-119">Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="6f30d-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="6f30d-120">*pfQOP* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="6f30d-121">Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.</span><span class="sxs-lookup"><span data-stu-id="6f30d-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="6f30d-122">Este parámetro puede ser la marca siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f30d-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="6f30d-123">Value</span><span class="sxs-lookup"><span data-stu-id="6f30d-123">Value</span></span>                  | <span data-ttu-id="6f30d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="6f30d-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6f30d-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="6f30d-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="6f30d-126">no se cifró el mensaje, pero se produjo un encabezado o finalizador.</span><span class="sxs-lookup"><span data-stu-id="6f30d-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="6f30d-127">KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</span><span class="sxs-lookup"><span data-stu-id="6f30d-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f30d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f30d-128">Return value</span></span>

<span data-ttu-id="6f30d-129">Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f30d-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="6f30d-130">Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6f30d-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="6f30d-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6f30d-131">Return code</span></span>                     | <span data-ttu-id="6f30d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f30d-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f30d-133">**s \_ E \_ mensaje incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="6f30d-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="6f30d-134">Los datos del búfer de entrada están incompletos.</span><span class="sxs-lookup"><span data-stu-id="6f30d-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="6f30d-135">La aplicación debe leer más datos del servidor y llamar de nuevo a [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="6f30d-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="6f30d-136">**s \_ E \_ fuera \_ de \_ secuencia**</span><span class="sxs-lookup"><span data-stu-id="6f30d-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="6f30d-137">No se recibió el mensaje en la secuencia correcta.</span><span class="sxs-lookup"><span data-stu-id="6f30d-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="6f30d-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f30d-138">Remarks</span></span>

<span data-ttu-id="6f30d-139">A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Kerberos)** y detectará que **DecryptMessage (Kerberos)** se ejecutó correctamente, pero los búferes de salida están vacíos.</span><span class="sxs-lookup"><span data-stu-id="6f30d-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="6f30d-140">Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.</span><span class="sxs-lookup"><span data-stu-id="6f30d-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="6f30d-141">Para obtener información acerca de cómo interoperar con GSSAPI, consulte [interoperabilidad de SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="6f30d-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="6f30d-142">**Windows XP:** Esta función también se conocía como **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="6f30d-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="6f30d-143">Las aplicaciones ahora deben usar **DecryptMessage (Kerberos)** solamente.</span><span class="sxs-lookup"><span data-stu-id="6f30d-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f30d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f30d-144">Requirements</span></span>

| <span data-ttu-id="6f30d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f30d-145">Requirement</span></span> | <span data-ttu-id="6f30d-146">Value</span><span class="sxs-lookup"><span data-stu-id="6f30d-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6f30d-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f30d-147">Minimum supported client</span></span> | <span data-ttu-id="6f30d-148">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="6f30d-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f30d-149">Minimum supported server</span></span> | <span data-ttu-id="6f30d-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f30d-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="6f30d-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f30d-151">Header</span></span>                   | <span data-ttu-id="6f30d-152">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="6f30d-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="6f30d-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f30d-153">Library</span></span>                  | <span data-ttu-id="6f30d-154">SECUR32. lib</span><span class="sxs-lookup"><span data-stu-id="6f30d-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="6f30d-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f30d-155">DLL</span></span>                      | <span data-ttu-id="6f30d-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="6f30d-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="6f30d-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f30d-157">See also</span></span>

- [<span data-ttu-id="6f30d-158">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="6f30d-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="6f30d-159">**EncryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="6f30d-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="6f30d-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f30d-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="6f30d-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="6f30d-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
