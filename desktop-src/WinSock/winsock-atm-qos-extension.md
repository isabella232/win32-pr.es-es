---
description: En esta sección se describe la estructura de calidad de servicio (QOS) específica del protocolo para ATM, que se encuentra en el campo ProviderSpecific de la estructura de QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensión QoS de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154240"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="55da8-103">Extensión QoS de ATM de Winsock</span><span class="sxs-lookup"><span data-stu-id="55da8-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="55da8-104">En esta sección se describe la estructura de calidad de servicio ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) específica del protocolo para ATM, que se encuentra en el campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) de la estructura de **QoS** .</span><span class="sxs-lookup"><span data-stu-id="55da8-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="55da8-105">Tenga en cuenta que el uso de esta estructura **QoS** específica de ATM es opcional para los clientes de Windows Sockets 2, y el proveedor de servicios ATM es necesario para asignar la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) genérica a los elementos de información Q. 2931 adecuados.</span><span class="sxs-lookup"><span data-stu-id="55da8-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="55da8-106">Sin embargo, si se especifican tanto la estructura **FLOWSPEC** genérica como la estructura de **QoS** específica de ATM, el valor especificado en la estructura **QoS** específica de ATM debería tener prioridad en caso de que se produzcan conflictos.</span><span class="sxs-lookup"><span data-stu-id="55da8-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="55da8-107">Consulte la sección 2,7 de la especificación de la API de Windows Sockets 2 para obtener más información sobre las provisiones de QoS y la estructura **FLOWSPEC** .</span><span class="sxs-lookup"><span data-stu-id="55da8-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="55da8-108">La estructura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica del protocolo para ATM es una concatenación de estructuras Q. 2931 Information Element (IE), que se definen en el siguiente texto.</span><span class="sxs-lookup"><span data-stu-id="55da8-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="55da8-109">Si una aplicación omite un e/o que el UNI 3. x asigna, el proveedor de servicios debe insertar un valor predeterminado razonable, teniendo en cuenta la información de la estructura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) si es aplicable.</span><span class="sxs-lookup"><span data-stu-id="55da8-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="55da8-110">La administración de s repetida depende del propio IE.</span><span class="sxs-lookup"><span data-stu-id="55da8-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="55da8-111">Si se repite una IE y es una que se puede repetir según la especificación UNI del Foro de ATM, el proveedor debe administrarla correctamente.</span><span class="sxs-lookup"><span data-stu-id="55da8-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="55da8-112">En este caso, el orden de la lista determina el orden de las preferencias, con los elementos que aparecen anteriormente en la lista que son más preferidos.</span><span class="sxs-lookup"><span data-stu-id="55da8-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="55da8-113">Si se repite una instancia de IE y esto no se permite por especificación UNI del Foro de ATM, el proveedor puede producir un error en la solicitud del cliente (la opción preferida) o usar el último IE de ese tipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="55da8-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="55da8-114">Cada estructura individual de IE tiene el formato de la siguiente manera y se identifica mediante el campo **IEType** :</span><span class="sxs-lookup"><span data-stu-id="55da8-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="55da8-115">Los valores válidos para el campo **IEType** se definen como:</span><span class="sxs-lookup"><span data-stu-id="55da8-115">Legal values for the **IEType** field are defined as:</span></span>

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

<span data-ttu-id="55da8-116">El campo de **IE** está superpuesto por una estructura específica de IE y el campo **IELength** es la longitud total en bytes de la estructura de IE, incluidos los campos **IEType** y **IELength** .</span><span class="sxs-lookup"><span data-stu-id="55da8-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="55da8-117">La semántica y los valores válidos para cada elemento de estas estructuras de Internet Explorer son por cada especificación UNI 3. x de ATM.</span><span class="sxs-lookup"><span data-stu-id="55da8-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="55da8-118">\_El campo \_ de SAP ausente se puede usar para los elementos que son opcionales para una estructura de IE determinada, según la especificación de UNI 3. x de ATM.</span><span class="sxs-lookup"><span data-stu-id="55da8-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
