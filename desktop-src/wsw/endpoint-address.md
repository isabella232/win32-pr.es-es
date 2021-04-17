---
title: Dirección del extremo
description: Una dirección de punto de conexión representa la dirección de un servicio en la red.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Servicios Web de la dirección de extremo para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558018"
---
# <a name="endpoint-address"></a><span data-ttu-id="17e9a-106">Dirección del extremo</span><span class="sxs-lookup"><span data-stu-id="17e9a-106">Endpoint Address</span></span>

<span data-ttu-id="17e9a-107">Una dirección de punto de conexión representa la dirección de un servicio en la red.</span><span class="sxs-lookup"><span data-stu-id="17e9a-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="17e9a-108">Al abrir un [canal](channel.md)mediante una llamada a la función [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , debe proporcionar la dirección del punto de conexión del servicio con el que se va a comunicar, así como especificar el canal que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="17e9a-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="17e9a-109">Una dirección de punto de conexión consta de:</span><span class="sxs-lookup"><span data-stu-id="17e9a-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="17e9a-110">una [dirección URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="17e9a-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="17e9a-111">un conjunto de encabezados (opcional)</span><span class="sxs-lookup"><span data-stu-id="17e9a-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="17e9a-112">un conjunto de extensiones (opcional)</span><span class="sxs-lookup"><span data-stu-id="17e9a-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="17e9a-113">[identidad](endpoint-identity.md) opcional que representa la identidad de seguridad del servicio.</span><span class="sxs-lookup"><span data-stu-id="17e9a-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="17e9a-114">Cuando se trata de un mensaje, la dirección URL se convierte en el encabezado "para" del mensaje.</span><span class="sxs-lookup"><span data-stu-id="17e9a-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="17e9a-115">Todos los encabezados que forman parte de la dirección del punto de conexión también se agregan al mensaje.</span><span class="sxs-lookup"><span data-stu-id="17e9a-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Diagrama que muestra los encabezados de dirección de extremo que se agregan a un mensaje.](images/endpointaddress.png)

<span data-ttu-id="17e9a-117">Los canales abordan automáticamente los mensajes que se envían mediante la estructura de [**\_ \_ direcciones del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que se pasó a [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span><span class="sxs-lookup"><span data-stu-id="17e9a-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="17e9a-118">También puede usar la función [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) para invalidar este comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="17e9a-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="17e9a-119">Cuando se pasa la [**\_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) como parámetro, las funciones [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) y [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) crean una copia del parámetro de dirección del **punto de \_ conexión \_ de WS** en la memoria y su tamaño está limitado por 65536 bytes.</span><span class="sxs-lookup"><span data-stu-id="17e9a-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="17e9a-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) no tiene esta limitación porque no requiere la creación de una copia del parámetro de **\_ \_ dirección del punto de conexión de WS** .</span><span class="sxs-lookup"><span data-stu-id="17e9a-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="17e9a-121">Las extensiones especificadas en el campo **extensiones** de la [**dirección del punto de \_ conexión \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) no se usan para direccionar el mensaje, sino que son un mecanismo de extensibilidad que se puede usar para proporcionar información adicional (por ejemplo, metadatos) sobre el servicio.</span><span class="sxs-lookup"><span data-stu-id="17e9a-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="17e9a-122">Las extensiones comunes se pueden leer con la función [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .</span><span class="sxs-lookup"><span data-stu-id="17e9a-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="17e9a-123">El campo de identidad opcional de la dirección del extremo puede incluir, por ejemplo, el nombre DNS del equipo en el que se ejecuta el servicio o el UPN de la cuenta de Windows con la que se está ejecutando el servicio.</span><span class="sxs-lookup"><span data-stu-id="17e9a-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="17e9a-124">El campo identidad no se utiliza para direccionar el mensaje, pero se puede usar para obtener un token de seguridad para el servicio (por ejemplo, para obtener un vale de Kerberos para el UPN de destino) y para comprobar la identidad de las respuestas del servicio (por ejemplo, una identidad DNS utilizada para las comprobaciones de nombres en el certificado de servicio devuelto durante SSL).</span><span class="sxs-lookup"><span data-stu-id="17e9a-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="17e9a-125">Las direcciones de punto de conexión se pueden leer y escribir mediante la [serialización](serialization.md) con el valor de enumeración de **\_ tipo de \_ dirección \_ de extremo WS** de [**\_ tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="17e9a-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="17e9a-126">Nota para serializar una dirección de extremo, debe conocer la versión de la especificación utilizada para los encabezados de direccionamiento, tal como se especifica en la enumeración de la [**versión de WS \_ Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="17e9a-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




