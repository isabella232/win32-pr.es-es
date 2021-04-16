---
title: Excepciones de Firewall necesarias para Teredo
description: Para que una aplicación reciba tráfico Teredo, la aplicación debe tener permiso para recibir tráfico IPv6 en el firewall del host y la aplicación debe establecer la opción de socket nivel de protección IPV6 en \_ \_ "nivel de protección no \_ \_ restringido".
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685776"
---
# <a name="required-firewall-exceptions-for-teredo"></a><span data-ttu-id="554f0-103">Excepciones de Firewall necesarias para Teredo</span><span class="sxs-lookup"><span data-stu-id="554f0-103">Required Firewall Exceptions for Teredo</span></span>

<span data-ttu-id="554f0-104">Para que una aplicación reciba tráfico Teredo, la aplicación debe tener permiso para recibir tráfico IPv6 en el firewall del host y la aplicación debe establecer la opción de socket [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) en "nivel de protección no \_ \_ restringido".</span><span class="sxs-lookup"><span data-stu-id="554f0-104">For an application to receive Teredo traffic, the application must be permitted to receive IPv6 traffic in the host firewall, and the application is required to set the socket option [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) to 'PROTECTION\_LEVEL\_UNRESTRICTED'.</span></span> <span data-ttu-id="554f0-105">Para habilitar este tipo de escenario, se deben implementar las excepciones de firewall que se detallan en este documento.</span><span class="sxs-lookup"><span data-stu-id="554f0-105">To enable this type of scenario, the firewall exceptions detailed in this document must be implemented.</span></span>

<span data-ttu-id="554f0-106">Las siguientes configuraciones de firewall son necesarias para garantizar una interoperación fluida entre un firewall y Teredo:</span><span class="sxs-lookup"><span data-stu-id="554f0-106">The following firewall configurations are required to ensure smooth interoperation between a firewall and Teredo:</span></span>

-   <span data-ttu-id="554f0-107">El firewall del cliente debe permitir la resolución de teredo.ipv6.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="554f0-107">The client firewall must allow resolution of teredo.ipv6.microsoft.com.</span></span>
-   <span data-ttu-id="554f0-108">El puerto UDP 3544 debe estar abierto para asegurarse de que los clientes Teredo puedan comunicarse correctamente con el servidor Teredo.</span><span class="sxs-lookup"><span data-stu-id="554f0-108">UDP Port 3544 must be open to ensure that Teredo clients can successfully communicate with the Teredo server.</span></span>
-   <span data-ttu-id="554f0-109">El Firewall debe recuperar los puertos UDP dinámicos usados por el servicio Teredo en el equipo local llamando a la función [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . los puertos pertinentes son del tipo FWPM \_ del sistema \_ \_ Teredo.</span><span class="sxs-lookup"><span data-stu-id="554f0-109">The firewall must retrieve dynamic UDP ports used by Teredo service on the local machine by calling the [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) function; relevant ports are of type FWPM\_SYSTEM\_PORT\_TEREDO.</span></span> <span data-ttu-id="554f0-110">La función **FwpmSystemPortsGet0** debe implementarse en lugar de las funciones [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) o [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) en desuso.</span><span class="sxs-lookup"><span data-stu-id="554f0-110">The **FwpmSystemPortsGet0** function should be implemented in place of the now deprecated [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) or [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) functions.</span></span>
-   <span data-ttu-id="554f0-111">El Firewall permite al sistema enviar y recibir paquetes UDP/IPv4 al puerto UDP 1900 en la subred local, ya que esto permite que el tráfico de detección de UPnP fluya y tenga el potencial de mejorar las tasas de conectividad.</span><span class="sxs-lookup"><span data-stu-id="554f0-111">The firewall permits the system to send and receive UDP/IPv4 packets to UDP port 1900 on the local subnet as this allows UPnP discovery traffic to flow and has the potential to improve connectivity rates.</span></span>
    > [!Note]  
    > <span data-ttu-id="554f0-112">Si no se cumple esta condición, se introduce la posibilidad de que se produzcan problemas de compatibilidad que impliquen la comunicación entre determinados tipos de NAT; específicamente entre NAT simétricos y NAT restringidos.</span><span class="sxs-lookup"><span data-stu-id="554f0-112">If this condition is not met, the potential for scenarios to encounter compatibility issues involving communication between certain NAT types is introduced; specifically between Symmetric NATs and Restricted NATs.</span></span> <span data-ttu-id="554f0-113">Aunque los NAT simétricos son populares en las zonas activas y los NAT restringidos son populares en casa, la comunicación entre los dos tiene la posibilidad de que se produzca un error en el lado de la NAT restringida.</span><span class="sxs-lookup"><span data-stu-id="554f0-113">While Symmetric NATs are popular in hotspots and Restricted NATs are popular in homes, communication between the two has the potential to fault on the side of the Restricted NAT.</span></span>

     

-   <span data-ttu-id="554f0-114">Las excepciones ICMPv6 entrante y saliente "solicitud de Eco" y "respuesta de Eco" deben estar habilitadas.</span><span class="sxs-lookup"><span data-stu-id="554f0-114">Incoming and outgoing ICMPv6 "Echo Request" and "Echo Reply" exceptions must be enabled.</span></span> <span data-ttu-id="554f0-115">Estas excepciones son necesarias para garantizar que un cliente Teredo pueda actuar como una retransmisión específica del host Teredo.</span><span class="sxs-lookup"><span data-stu-id="554f0-115">These exceptions are necessary to ensure that a Teredo client can act as a Teredo host-specific relay.</span></span> <span data-ttu-id="554f0-116">Una retransmisión específica del host Teredo se puede identificar mediante la dirección IPv6 nativa adicional o una dirección 6to4 suministrada con la dirección Teredo.</span><span class="sxs-lookup"><span data-stu-id="554f0-116">A Teredo host-specific relay can be identified by the additional native IPv6 address or a 6to4 address supplied with the Teredo address.</span></span>

<span data-ttu-id="554f0-117">Los firewalls de cliente deben admitir los siguientes mensajes de error de ICMPv6 y funciones de detección por RFC 4443:</span><span class="sxs-lookup"><span data-stu-id="554f0-117">Client firewalls must support the following ICMPv6 error messages and discovery functions per RFC 4443:</span></span>



| <span data-ttu-id="554f0-118">Código</span><span class="sxs-lookup"><span data-stu-id="554f0-118">Code</span></span>    | <span data-ttu-id="554f0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="554f0-119">Description</span></span>                                    |
|---------|------------------------------------------------|
| <span data-ttu-id="554f0-120">135/136</span><span class="sxs-lookup"><span data-stu-id="554f0-120">135/136</span></span> | <span data-ttu-id="554f0-121">Aviso y solicitud de vecino ICMPV6</span><span class="sxs-lookup"><span data-stu-id="554f0-121">ICMPV6 Neighbor Solicitation and Advertisement</span></span> |
| <span data-ttu-id="554f0-122">133/134</span><span class="sxs-lookup"><span data-stu-id="554f0-122">133/134</span></span> | <span data-ttu-id="554f0-123">Solicitud y anuncio de enrutador</span><span class="sxs-lookup"><span data-stu-id="554f0-123">Router Solicitation and Advertisement</span></span>          |
| <span data-ttu-id="554f0-124">128/129</span><span class="sxs-lookup"><span data-stu-id="554f0-124">128/129</span></span> | <span data-ttu-id="554f0-125">Solicitud de eco ICMPV6 y respuesta</span><span class="sxs-lookup"><span data-stu-id="554f0-125">ICMPV6 Echo Request and Reply</span></span>                  |
| <span data-ttu-id="554f0-126">1</span><span class="sxs-lookup"><span data-stu-id="554f0-126">1</span></span>       | <span data-ttu-id="554f0-127">Destino no accesible</span><span class="sxs-lookup"><span data-stu-id="554f0-127">Destination Unreachable</span></span>                        |
| <span data-ttu-id="554f0-128">2</span><span class="sxs-lookup"><span data-stu-id="554f0-128">2</span></span>       | <span data-ttu-id="554f0-129">Paquete demasiado grande</span><span class="sxs-lookup"><span data-stu-id="554f0-129">Packet Too Large</span></span>                               |
| <span data-ttu-id="554f0-130">3</span><span class="sxs-lookup"><span data-stu-id="554f0-130">3</span></span>       | <span data-ttu-id="554f0-131">Tiempo superado</span><span class="sxs-lookup"><span data-stu-id="554f0-131">Time Exceeded</span></span>                                  |
| <span data-ttu-id="554f0-132">4</span><span class="sxs-lookup"><span data-stu-id="554f0-132">4</span></span>       | <span data-ttu-id="554f0-133">Parámetro no válido</span><span class="sxs-lookup"><span data-stu-id="554f0-133">Invalid Parameter</span></span>                              |



 

<span data-ttu-id="554f0-134">Si estos mensajes no se pueden permitir específicamente, la exención de todos los mensajes ICMPv6 debe estar habilitada en el firewall.</span><span class="sxs-lookup"><span data-stu-id="554f0-134">If these messages cannot be specifically allowed, then the exemption of all ICMPv6 messages should be enabled on the firewall.</span></span> <span data-ttu-id="554f0-135">Además, es posible que el firewall del host Observe que los paquetes clasificados por los códigos 135/136 o 133/134 proceden del servicio de modo de usuario **Iphlpsvc** y no de la pila.</span><span class="sxs-lookup"><span data-stu-id="554f0-135">Additionally, the host firewall may notice that the packets classified by codes 135/136 or 133/134 originate from, or are targeted to, the user mode service **iphlpsvc** and not from the stack.</span></span> <span data-ttu-id="554f0-136">El firewall del host no debe quitar estos paquetes.</span><span class="sxs-lookup"><span data-stu-id="554f0-136">These packets must not be dropped by the host firewall.</span></span> <span data-ttu-id="554f0-137">El servicio Teredo se implementa principalmente en el servicio auxiliar IP "modo de usuario".</span><span class="sxs-lookup"><span data-stu-id="554f0-137">The Teredo service is implemented primarily within the 'user mode' IP Helper service.</span></span>

<span data-ttu-id="554f0-138">Con la API de Firewall de Windows de [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) para enumerar todas las reglas con la marca de cruce seguro del perímetro, todas las aplicaciones que desean escuchar el tráfico no solicitado se enumeran para la excepción de Firewall.</span><span class="sxs-lookup"><span data-stu-id="554f0-138">Using the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows Firewall API to enumerate all rules with the Edge Traversal flag set, all applications that want to listen for unsolicited traffic are enumerated for the firewall exception.</span></span> <span data-ttu-id="554f0-139">La información específica sobre el uso de la opción de cruce seguro del perímetro se detalla en [recibir tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="554f0-139">Specific information regarding the use of the Edge Traversal option is detailed in [Receiving Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="554f0-140">Las devoluciones de llamada no están asociadas al código de enumeración de ejemplo siguiente; se recomienda encarecidamente que los firewalls de terceros realicen la enumeración periódicamente, o siempre que el Firewall detecte una nueva aplicación que intente pasar por el firewall.</span><span class="sxs-lookup"><span data-stu-id="554f0-140">Callbacks are not associated with the following sample enumeration code; it is strongly recommended that third party firewalls perform the enumeration periodically, or whenever the firewall detects a new application attempting to go through the firewall.</span></span>


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 