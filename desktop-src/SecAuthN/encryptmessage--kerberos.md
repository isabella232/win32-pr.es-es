---
description: Cifra un mensaje para ofrecer privacidad mediante Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Función EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278590"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="1b27b-103">Función EncryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="1b27b-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="1b27b-104">La función **EncryptMessage (Kerberos)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b27b-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="1b27b-105">**EncryptMessage (Kerberos)** permite que una aplicación Elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido.</span><span class="sxs-lookup"><span data-stu-id="1b27b-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="1b27b-106">La función **EncryptMessage (Kerberos)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="1b27b-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="1b27b-107">Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.</span><span class="sxs-lookup"><span data-stu-id="1b27b-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="1b27b-108">Se puede llamar a **EncryptMessage (Kerberos)** y [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando.</span><span class="sxs-lookup"><span data-stu-id="1b27b-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="1b27b-109">Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.</span><span class="sxs-lookup"><span data-stu-id="1b27b-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b27b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b27b-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="1b27b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b27b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b27b-112">*phContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b27b-113">Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b27b-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="1b27b-114">*fQOP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b27b-115">Marcas específicas del paquete que indican la calidad de la protección.</span><span class="sxs-lookup"><span data-stu-id="1b27b-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="1b27b-116">Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b27b-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="1b27b-117">Este parámetro puede ser la marca siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b27b-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="1b27b-118">Value</span><span class="sxs-lookup"><span data-stu-id="1b27b-118">Value</span></span></th><th><span data-ttu-id="1b27b-119">Significado</span><span class="sxs-lookup"><span data-stu-id="1b27b-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="1b27b-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1b27b-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="1b27b-121">Producir un encabezado o un finalizador, pero no cifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b27b-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="1b27b-122">KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</span><span class="sxs-lookup"><span data-stu-id="1b27b-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="1b27b-123">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b27b-124">Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="1b27b-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="1b27b-125">En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="1b27b-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="1b27b-126">Ese búfer contiene el mensaje que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="1b27b-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="1b27b-127">El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1b27b-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="1b27b-128">La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="1b27b-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="1b27b-129">La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ Stream \_ sizes).</span><span class="sxs-lookup"><span data-stu-id="1b27b-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="1b27b-130">Las aplicaciones que no usan SSL deben proporcionar un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SecBuffer \_ padding.</span><span class="sxs-lookup"><span data-stu-id="1b27b-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="1b27b-131">*MessageSeqNo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b27b-132">Número de secuencia que la aplicación de transporte asignó al mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b27b-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="1b27b-133">Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b27b-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b27b-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b27b-134">Return value</span></span>

<span data-ttu-id="1b27b-135">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b27b-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1b27b-136">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1b27b-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="1b27b-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1b27b-137">Return code</span></span>                                                                                                    | <span data-ttu-id="1b27b-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b27b-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b27b-139"><dt>**búfer de s \_ E s \_ \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="1b27b-140">El búfer de salida es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="1b27b-140">The output buffer is too small.</span></span> <span data-ttu-id="1b27b-141">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1b27b-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="1b27b-142"><dt>**SEC \_ E \_ contexto \_ expirado**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="1b27b-143">La aplicación hace referencia a un contexto que ya se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="1b27b-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="1b27b-144">Una aplicación escrita correctamente no debe recibir este error.</span><span class="sxs-lookup"><span data-stu-id="1b27b-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="1b27b-145"><dt>**s \_ E \_ \_ sistema criptográfico \_ no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="1b27b-146">No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1b27b-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="1b27b-147"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="1b27b-148">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="1b27b-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="1b27b-149"><dt>**s \_ E \_ identificador no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="1b27b-150">Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="1b27b-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="1b27b-151"><dt>**s \_ E \_ token no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="1b27b-152">No \_ se encontró ningún búfer de tipo de datos SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="1b27b-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1b27b-153"><dt>**s \_ E \_ QOP \_ no \_ admitidos**</dt></span><span class="sxs-lookup"><span data-stu-id="1b27b-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="1b27b-154">La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b27b-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="1b27b-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b27b-155">Remarks</span></span>

<span data-ttu-id="1b27b-156">La función **EncryptMessage (Kerberos)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b27b-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="1b27b-157">Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="1b27b-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="1b27b-158">La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1b27b-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="1b27b-159">El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.</span><span class="sxs-lookup"><span data-stu-id="1b27b-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="1b27b-160">Estos búferes se deben proporcionar en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="1b27b-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="1b27b-161">Tipo de búfer</span><span class="sxs-lookup"><span data-stu-id="1b27b-161">Buffer type</span></span>                           | <span data-ttu-id="1b27b-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b27b-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b27b-163">< de encabezado de \_ flujo de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="1b27b-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="1b27b-164">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="1b27b-164">Used internally.</span></span> <span data-ttu-id="1b27b-165">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="1b27b-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="1b27b-166">datos de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="1b27b-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="1b27b-167">Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="1b27b-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="1b27b-168">\_finalizador de flujo SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="1b27b-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="1b27b-169">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="1b27b-169">Used internally.</span></span> <span data-ttu-id="1b27b-170">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="1b27b-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="1b27b-171">SECBUFFER \_ vacío</span><span class="sxs-lookup"><span data-stu-id="1b27b-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="1b27b-172">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="1b27b-172">Used internally.</span></span> <span data-ttu-id="1b27b-173">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="1b27b-173">No initialization required.</span></span> <span data-ttu-id="1b27b-174">El tamaño puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b27b-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="1b27b-175">Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="1b27b-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="1b27b-176">**Windows XP:** Esta función también se conocía como **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="1b27b-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="1b27b-177">Las aplicaciones ahora deben usar **EncryptMessage (Kerberos)** solamente.</span><span class="sxs-lookup"><span data-stu-id="1b27b-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b27b-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b27b-178">Requirements</span></span>

| <span data-ttu-id="1b27b-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b27b-179">Requirement</span></span> | <span data-ttu-id="1b27b-180">Value</span><span class="sxs-lookup"><span data-stu-id="1b27b-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="1b27b-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b27b-181">Minimum supported client</span></span> | <span data-ttu-id="1b27b-182">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="1b27b-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b27b-183">Minimum supported server</span></span> | <span data-ttu-id="1b27b-184">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b27b-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="1b27b-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b27b-185">Header</span></span>                   | <span data-ttu-id="1b27b-186">SSPI. h (incluir Security. h)</span><span class="sxs-lookup"><span data-stu-id="1b27b-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="1b27b-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b27b-187">Library</span></span>                  | <span data-ttu-id="1b27b-188">SECUR32. lib</span><span class="sxs-lookup"><span data-stu-id="1b27b-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="1b27b-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b27b-189">DLL</span></span>                      | <span data-ttu-id="1b27b-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="1b27b-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="1b27b-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b27b-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b27b-192">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="1b27b-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="1b27b-193">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="1b27b-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="1b27b-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="1b27b-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="1b27b-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="1b27b-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="1b27b-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="1b27b-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="1b27b-197">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="1b27b-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="1b27b-198">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="1b27b-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
