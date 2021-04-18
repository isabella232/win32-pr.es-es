---
description: Cifra un mensaje para ofrecer privacidad mediante síntesis.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Función EncryptMessage (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720323"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="aa03e-103">EncryptMessage (síntesis) (función)</span><span class="sxs-lookup"><span data-stu-id="aa03e-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="aa03e-104">La función **EncryptMessage (síntesis)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa03e-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="aa03e-105">**EncryptMessage (síntesis)** permite que la aplicación Elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido.</span><span class="sxs-lookup"><span data-stu-id="aa03e-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="aa03e-106">La función **EncryptMessage (síntesis)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="aa03e-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="aa03e-107">Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.</span><span class="sxs-lookup"><span data-stu-id="aa03e-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="aa03e-108">Esta función solo está disponible como un mecanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="aa03e-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="aa03e-109">Se puede llamar a **EncryptMessage (digest)** y [**DecryptMessage (digest)**](decryptmessage--digest.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando.</span><span class="sxs-lookup"><span data-stu-id="aa03e-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="aa03e-110">Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.</span><span class="sxs-lookup"><span data-stu-id="aa03e-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="aa03e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa03e-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="aa03e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa03e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa03e-113">*phContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa03e-114">Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa03e-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="aa03e-115">*fQOP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa03e-116">Marcas específicas del paquete que indican la calidad de la protección.</span><span class="sxs-lookup"><span data-stu-id="aa03e-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="aa03e-117">Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa03e-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="aa03e-118">Al usar el SSP de síntesis, este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="aa03e-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="aa03e-119">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa03e-120">Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="aa03e-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="aa03e-121">En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="aa03e-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="aa03e-122">Ese búfer contiene el mensaje que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="aa03e-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="aa03e-123">El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.</span><span class="sxs-lookup"><span data-stu-id="aa03e-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="aa03e-124">La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="aa03e-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="aa03e-125">La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) ( \_ tamaños de flujo SECPKG ATTR \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="aa03e-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="aa03e-126">Al usar el SSP de síntesis, debe haber un segundo búfer de tipo SECBUFFER \_ padding o sec \_ \_ Data buffer para almacenar la información de la [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) .</span><span class="sxs-lookup"><span data-stu-id="aa03e-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="aa03e-127">Para obtener el tamaño del búfer de salida, llame a la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) y especifique los tamaños de SECPKG \_ ATTR \_ .</span><span class="sxs-lookup"><span data-stu-id="aa03e-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="aa03e-128">La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="aa03e-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="aa03e-129">El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="aa03e-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="aa03e-130">Las aplicaciones que no usan SSL deben proporcionar un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SecBuffer \_ padding.</span><span class="sxs-lookup"><span data-stu-id="aa03e-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="aa03e-131">*MessageSeqNo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa03e-132">Número de secuencia que la aplicación de transporte asignó al mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa03e-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="aa03e-133">Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="aa03e-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="aa03e-134">Al usar el SSP de síntesis, este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="aa03e-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="aa03e-135">El SSP de síntesis administra la numeración de secuencias internamente.</span><span class="sxs-lookup"><span data-stu-id="aa03e-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa03e-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa03e-136">Return value</span></span>

<span data-ttu-id="aa03e-137">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa03e-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="aa03e-138">Si se produce un error en la función, devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="aa03e-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="aa03e-139">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aa03e-139">Return code</span></span>                                                                                                    | <span data-ttu-id="aa03e-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa03e-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa03e-141"><dt>**búfer de s \_ E s \_ \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="aa03e-142">El búfer de salida es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="aa03e-142">The output buffer is too small.</span></span> <span data-ttu-id="aa03e-143">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="aa03e-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="aa03e-144"><dt>**SEC \_ E \_ contexto \_ expirado**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="aa03e-145">La aplicación hace referencia a un contexto que ya se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="aa03e-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="aa03e-146">Una aplicación escrita correctamente no debe recibir este error.</span><span class="sxs-lookup"><span data-stu-id="aa03e-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="aa03e-147"><dt>**s \_ E \_ \_ sistema criptográfico \_ no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="aa03e-148">No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aa03e-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="aa03e-149"><dt>**s \_ E \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="aa03e-150">No hay suficiente memoria disponible para completar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="aa03e-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="aa03e-151"><dt>**s \_ E \_ identificador no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="aa03e-152">Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="aa03e-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="aa03e-153"><dt>**s \_ E \_ token no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="aa03e-154">No \_ se encontró ningún búfer de tipo de datos SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="aa03e-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="aa03e-155"><dt>**s \_ E \_ QOP \_ no \_ admitidos**</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="aa03e-156">La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa03e-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa03e-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa03e-157">Remarks</span></span>

<span data-ttu-id="aa03e-158">La función **EncryptMessage (síntesis)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa03e-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="aa03e-159">Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="aa03e-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="aa03e-160">La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa03e-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="aa03e-161">El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.</span><span class="sxs-lookup"><span data-stu-id="aa03e-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="aa03e-162">Cuando use el SSP de síntesis, obtenga el tamaño del búfer de salida mediante una llamada a la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) y especifique los tamaños de SECPKG \_ ATTR \_ .</span><span class="sxs-lookup"><span data-stu-id="aa03e-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="aa03e-163">La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="aa03e-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="aa03e-164">El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="aa03e-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="aa03e-165">Estos búferes se deben proporcionar en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="aa03e-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="aa03e-166">Tipo de búfer</span><span class="sxs-lookup"><span data-stu-id="aa03e-166">Buffer type</span></span>                           | <span data-ttu-id="aa03e-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa03e-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa03e-168">SECBUFFER \_ encabezado de secuencia \_</span><span class="sxs-lookup"><span data-stu-id="aa03e-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="aa03e-169">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="aa03e-169">Used internally.</span></span> <span data-ttu-id="aa03e-170">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="aa03e-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="aa03e-171">datos de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="aa03e-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="aa03e-172">Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="aa03e-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="aa03e-173">\_finalizador de flujo SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="aa03e-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="aa03e-174">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="aa03e-174">Used internally.</span></span> <span data-ttu-id="aa03e-175">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="aa03e-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="aa03e-176">SECBUFFER \_ vacío</span><span class="sxs-lookup"><span data-stu-id="aa03e-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="aa03e-177">Utilizado de forma interna.</span><span class="sxs-lookup"><span data-stu-id="aa03e-177">Used internally.</span></span> <span data-ttu-id="aa03e-178">No se requiere inicialización.</span><span class="sxs-lookup"><span data-stu-id="aa03e-178">No initialization required.</span></span> <span data-ttu-id="aa03e-179">El tamaño puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="aa03e-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="aa03e-180">Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="aa03e-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="aa03e-181">**Windows XP:** Esta función también se conocía como **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="aa03e-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="aa03e-182">Las aplicaciones ahora deben usar **EncryptMessage (digest)** solamente.</span><span class="sxs-lookup"><span data-stu-id="aa03e-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa03e-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa03e-183">Requirements</span></span>



| <span data-ttu-id="aa03e-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa03e-184">Requirement</span></span> | <span data-ttu-id="aa03e-185">Value</span><span class="sxs-lookup"><span data-stu-id="aa03e-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa03e-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa03e-186">Minimum supported client</span></span><br/> | <span data-ttu-id="aa03e-187">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="aa03e-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa03e-188">Minimum supported server</span></span><br/> | <span data-ttu-id="aa03e-189">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa03e-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="aa03e-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa03e-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa03e-191"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="aa03e-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa03e-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa03e-193"><dt>SECUR32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="aa03e-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa03e-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa03e-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa03e-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="aa03e-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa03e-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa03e-197">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="aa03e-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="aa03e-198">**AcceptSecurityContext (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="aa03e-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="aa03e-199">**DecryptMessage (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="aa03e-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="aa03e-200">**InitializeSecurityContext (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="aa03e-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="aa03e-201">**QueryContextAttributes (Resumen)**</span><span class="sxs-lookup"><span data-stu-id="aa03e-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="aa03e-202">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="aa03e-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="aa03e-203">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="aa03e-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
