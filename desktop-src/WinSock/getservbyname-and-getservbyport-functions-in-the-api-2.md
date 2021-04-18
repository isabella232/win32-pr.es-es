---
description: Las funciones getservbyname y getservbyport usan la función WSALookupServiceBegin para consultar SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funciones getservbyname y getservbyport en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715125"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="57ff0-103">Funciones getservbyname y getservbyport en la API</span><span class="sxs-lookup"><span data-stu-id="57ff0-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="57ff0-104">Las funciones [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usan la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ SERVICEBYNAME como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="57ff0-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="57ff0-105">El miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) que se pasa a la función **WSALookupServiceBegin** hace referencia a una cadena para indicar el nombre del servicio o el puerto del servicio y, opcionalmente, el protocolo del servicio.</span><span class="sxs-lookup"><span data-stu-id="57ff0-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="57ff0-106">El formato de la cadena se muestra como FTP, TCP o 21/TCP o simplemente FTP.</span><span class="sxs-lookup"><span data-stu-id="57ff0-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="57ff0-107">La cadena no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="57ff0-107">The string is not case sensitive.</span></span> <span data-ttu-id="57ff0-108">La marca de barra diagonal, si está presente, separa el identificador de protocolo de la parte anterior de la cadena.</span><span class="sxs-lookup"><span data-stu-id="57ff0-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="57ff0-109">El \_32.dll Ws2 especificará LUP \_ devolverá el \_ BLOB y el proveedor de espacios de nombres colocará una estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente).</span><span class="sxs-lookup"><span data-stu-id="57ff0-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="57ff0-110">Los proveedores de espacios de nombres deben cumplir también estas otras \_ \_ \* marcas de devolución de LUP.</span><span class="sxs-lookup"><span data-stu-id="57ff0-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="57ff0-111">Marca</span><span class="sxs-lookup"><span data-stu-id="57ff0-111">Flag</span></span>              | <span data-ttu-id="57ff0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="57ff0-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ff0-113">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="57ff0-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="57ff0-114">Devuelve el miembro de **\_ nombre s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="57ff0-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="57ff0-115">\_tipo de valor devuelto LUP \_</span><span class="sxs-lookup"><span data-stu-id="57ff0-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="57ff0-116">Devuelve el GUID canónico en *lpServiceClassId* . se entiende que un servicio identificado como FTP o 21 puede estar en otro puerto de acuerdo con las convenciones establecidas localmente.</span><span class="sxs-lookup"><span data-stu-id="57ff0-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="57ff0-117">El parámetro de **\_ Puerto s** de la estructura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) debe indicar dónde se puede establecer contacto con el servicio en el entorno local.</span><span class="sxs-lookup"><span data-stu-id="57ff0-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="57ff0-118">El GUID canónico devuelto cuando el \_ tipo de valor devuelto LUP \_ está establecido debe ser uno de los GUID predefinidos de SVC. h que corresponde al número de puerto indicado en la estructura **SERVENT** .</span><span class="sxs-lookup"><span data-stu-id="57ff0-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="57ff0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57ff0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ff0-120">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="57ff0-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="57ff0-121">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="57ff0-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="57ff0-122">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="57ff0-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



