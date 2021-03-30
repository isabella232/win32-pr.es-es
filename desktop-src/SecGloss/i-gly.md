---
description: Contiene definiciones de términos de seguridad que comienzan por la letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082990"
---
# <a name="i-security-glossary"></a><span data-ttu-id="362fc-103">I (Glosario de seguridad)</span><span class="sxs-lookup"><span data-stu-id="362fc-103">I (Security Glossary)</span></span>

<span data-ttu-id="362fc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="362fc-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="362fc-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span><span class="sxs-lookup"><span data-stu-id="362fc-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-106">Servicios de software que admiten la creación, configuración y administración de sitios web, junto con otras funciones de Internet.</span><span class="sxs-lookup"><span data-stu-id="362fc-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="362fc-107">Internet Information Services incluyen el protocolo de transferencia de noticias en red (NNTP), el protocolo de transferencia de archivos (FTP) y el Protocolo simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="362fc-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="362fc-108">IIS incorpora varias funciones de seguridad, permite aplicaciones CGI y proporciona servidores Gopher y FTP.</span><span class="sxs-lookup"><span data-stu-id="362fc-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**suplantación**</span><span class="sxs-lookup"><span data-stu-id="362fc-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-110">Mecanismo que permite a un proceso de servidor ejecutarse mediante las credenciales de seguridad del cliente o algún otro usuario que use las credenciales.</span><span class="sxs-lookup"><span data-stu-id="362fc-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="362fc-111">Cuando el servidor suplanta al cliente, las operaciones realizadas por el servidor se realizan mediante las credenciales del cliente (suplantando al usuario).</span><span class="sxs-lookup"><span data-stu-id="362fc-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="362fc-112">La suplantación no permite que el servidor tenga acceso a los recursos remotos en nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="362fc-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="362fc-113">Esto requiere delegación.</span><span class="sxs-lookup"><span data-stu-id="362fc-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token de suplantación**</span><span class="sxs-lookup"><span data-stu-id="362fc-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-115">Un token de acceso que se ha creado para capturar la información de seguridad de un proceso de cliente, lo que permite a un servidor "suplantar" el proceso de cliente en operaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="362fc-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="362fc-116">Vea también [*token de acceso*](a-gly.md) y [*token principal*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="362fc-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="362fc-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**Vector de inicialización**</span><span class="sxs-lookup"><span data-stu-id="362fc-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-118">(IV) una secuencia de bytes aleatorios anexados al anverso del texto sin formato antes del cifrado mediante un cifrado de bloque.</span><span class="sxs-lookup"><span data-stu-id="362fc-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="362fc-119">Al agregar el vector de inicialización al principio del texto simple, se elimina la posibilidad de tener el bloque de texto cifrado inicial igual para dos mensajes cualesquiera.</span><span class="sxs-lookup"><span data-stu-id="362fc-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="362fc-120">Por ejemplo, si los mensajes siempre comienzan con un encabezado común (un membrete o una línea "de"), su texto cifrado inicial siempre será el mismo, suponiendo que se usó el mismo algoritmo criptográfico y clave simétrica.</span><span class="sxs-lookup"><span data-stu-id="362fc-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="362fc-121">La adición de un vector de inicialización aleatorio evita que esto suceda.</span><span class="sxs-lookup"><span data-stu-id="362fc-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**datos internos**</span><span class="sxs-lookup"><span data-stu-id="362fc-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-123">Cualquier dato codificado que se use como mensaje para otro mensaje codificado.</span><span class="sxs-lookup"><span data-stu-id="362fc-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="362fc-124">Por ejemplo, un mensaje con doble cifrado y su valor hash pueden ser los datos internos de un segundo mensaje.</span><span class="sxs-lookup"><span data-stu-id="362fc-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenido interno**</span><span class="sxs-lookup"><span data-stu-id="362fc-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-126">Datos que se han mejorado, como con una firma digital.</span><span class="sxs-lookup"><span data-stu-id="362fc-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="362fc-127">Este término se usa principalmente cuando se analizan datos mejorados en un \# mensaje PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="362fc-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integración**</span><span class="sxs-lookup"><span data-stu-id="362fc-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-129">La integridad y la precisión de un mensaje después de que se haya enviado o almacenado.</span><span class="sxs-lookup"><span data-stu-id="362fc-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID de integridad**</span><span class="sxs-lookup"><span data-stu-id="362fc-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-131">Un [*identificador de seguridad*](s-gly.md) (SID) que representa un nivel de integridad.</span><span class="sxs-lookup"><span data-stu-id="362fc-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="362fc-132">Un SID de integridad en la [*lista de control de acceso de sistema*](s-gly.md) (SACL) del descriptor de seguridad de un objeto especifica el nivel de integridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="362fc-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="362fc-133">Los SID de integridad de un token de acceso especifican el nivel de integridad del token.</span><span class="sxs-lookup"><span data-stu-id="362fc-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span><span class="sxs-lookup"><span data-stu-id="362fc-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-135">Un nivel de solicitud de interrupción (IRQL) define la prioridad de hardware en la que un procesador funciona en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="362fc-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="362fc-136">En el Modelo de controlador de Windows, se puede interrumpir un subproceso que se ejecuta en un IRQL bajo para ejecutar código en una IRQL superior.</span><span class="sxs-lookup"><span data-stu-id="362fc-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="362fc-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**CUARTA**</span><span class="sxs-lookup"><span data-stu-id="362fc-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="362fc-138">Consulte *Vector de inicialización*.</span><span class="sxs-lookup"><span data-stu-id="362fc-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



