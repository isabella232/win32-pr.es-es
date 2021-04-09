---
title: Fragmento
description: Use el paquete de fragmento para enviar al servidor un fragmento del archivo de carga.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragmento
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149094"
---
# <a name="fragment"></a><span data-ttu-id="9bb15-104">Fragmento</span><span class="sxs-lookup"><span data-stu-id="9bb15-104">Fragment</span></span>

<span data-ttu-id="9bb15-105">Use el paquete de **fragmento** para enviar al servidor un fragmento del archivo de carga.</span><span class="sxs-lookup"><span data-stu-id="9bb15-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="9bb15-106">Encabezados</span><span class="sxs-lookup"><span data-stu-id="9bb15-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="9bb15-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post bits</span><span class="sxs-lookup"><span data-stu-id="9bb15-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-108">Verbo específico de BITS que identifica este paquete en el servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="9bb15-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="9bb15-109">Reemplace Remote-URL por el URI absoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="9bb15-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="9bb15-110">Normalmente, reemplace Remote-URL por el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9bb15-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="9bb15-111">Para conocer las consideraciones sobre el equilibrio de carga de red, consulte el encabezado BITS-host-ID en el paquete de [**creación de sesión**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb15-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-paquete-tipo</span><span class="sxs-lookup"><span data-stu-id="9bb15-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-113">Identifica este paquete de solicitud como un paquete de fragmento.</span><span class="sxs-lookup"><span data-stu-id="9bb15-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Identificador de sesión BITS</span><span class="sxs-lookup"><span data-stu-id="9bb15-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-115">GUID de cadena que identifica la sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9bb15-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="9bb15-116">Reemplace {GUID} por el identificador de sesión que devuelve el servidor en el paquete de respuesta [**de confirmación para creación de sesión**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb15-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nombre de contenido</span><span class="sxs-lookup"><span data-stu-id="9bb15-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-118">Especifique este encabezado solo con el fragmento inicial.</span><span class="sxs-lookup"><span data-stu-id="9bb15-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="9bb15-119">Reemplace FILENAME por el nombre del archivo local del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9bb15-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="9bb15-120">El nombre no incluye la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9bb15-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Longitud de contenido</span><span class="sxs-lookup"><span data-stu-id="9bb15-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-122">Reemplace length por el número de bytes enviados en el cuerpo del fragmento.</span><span class="sxs-lookup"><span data-stu-id="9bb15-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span><span class="sxs-lookup"><span data-stu-id="9bb15-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-124">Indica al servidor dónde aplicar el intervalo en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9bb15-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="9bb15-125">Reemplace Range con los desplazamientos inicial y final del intervalo del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9bb15-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="9bb15-126">Los desplazamientos son de base cero.</span><span class="sxs-lookup"><span data-stu-id="9bb15-126">The offsets are zero-based.</span></span> <span data-ttu-id="9bb15-127">Si el intervalo especificado se superpone a un intervalo existente, BITS solo escribe la parte no superpuesta del intervalo. BITS no sobrescribe el contenido existente.</span><span class="sxs-lookup"><span data-stu-id="9bb15-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="9bb15-128">Por ejemplo, si el primer paquete contenía el intervalo comprendido entre 0 y 100 y el segundo paquete contenía el intervalo de 50 a 150, BITS escribe solo los bytes 101 a 150 del segundo paquete.</span><span class="sxs-lookup"><span data-stu-id="9bb15-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="9bb15-129">Reemplace total-length por el número total de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="9bb15-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="9bb15-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codificación de contenido</span><span class="sxs-lookup"><span data-stu-id="9bb15-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="9bb15-131">Reemplace la codificación con el tipo de codificación que el cliente usa en el fragmento.</span><span class="sxs-lookup"><span data-stu-id="9bb15-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="9bb15-132">El cliente debe usar la codificación que el servidor identifica en el encabezado Accept-Encoding del paquete de respuesta de [**confirmación de creación de sesión**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb15-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="9bb15-133">El servidor usa el tipo de codificación para descodificar el fragmento.</span><span class="sxs-lookup"><span data-stu-id="9bb15-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="9bb15-134">Todos los fragmentos deben especificar la misma codificación.</span><span class="sxs-lookup"><span data-stu-id="9bb15-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="9bb15-135">No envíe este encabezado si el tipo de codificación es Identity.</span><span class="sxs-lookup"><span data-stu-id="9bb15-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="9bb15-136">El servidor BITS solo admite la codificación de identidad.</span><span class="sxs-lookup"><span data-stu-id="9bb15-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bb15-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bb15-137">Remarks</span></span>

<span data-ttu-id="9bb15-138">El fragmento es un intervalo de bytes enviados en el cuerpo del paquete.</span><span class="sxs-lookup"><span data-stu-id="9bb15-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="9bb15-139">El cliente envía los fragmentos en orden secuencial a partir del desplazamiento cero; el servidor no realiza un seguimiento de los intervalos no contiguos.</span><span class="sxs-lookup"><span data-stu-id="9bb15-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="9bb15-140">Si el cliente envía intervalos no contiguos, el servidor devuelve un código de retorno HTTP 416 (intervalo no se puede satisfacer) en la [**confirmación para la respuesta de fragmento**](ack-for-fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb15-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="9bb15-141">Los encabezados Content-*xxxx* son encabezados HTTP 1,1 estándar.</span><span class="sxs-lookup"><span data-stu-id="9bb15-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="9bb15-142">Para obtener más información sobre los encabezados Content-*xxxx* , vea la especificación [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="9bb15-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bb15-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bb15-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb15-144">**Confirmación para fragmento**</span><span class="sxs-lookup"><span data-stu-id="9bb15-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="9bb15-145">**Sesión de cierre**</span><span class="sxs-lookup"><span data-stu-id="9bb15-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="9bb15-146">**Crear sesión**</span><span class="sxs-lookup"><span data-stu-id="9bb15-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




