---
title: Excepciones de firewall necesarias para Teredo
description: Para que una aplicación reciba tráfico de Teredo, se debe permitir que la aplicación reciba tráfico IPv6 en el firewall del host y la aplicación debe establecer la opción de socket IPV6 PROTECTION LEVEL en \_ \_ "PROTECTION \_ LEVEL \_ UNRESTRICTED".
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243537"
---
# <a name="required-firewall-exceptions-for-teredo"></a>Excepciones de firewall necesarias para Teredo

Para que una aplicación reciba tráfico de Teredo, se debe permitir que la aplicación reciba tráfico IPv6 en el firewall del host y la aplicación debe establecer la opción de socket [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) en "PROTECTION \_ LEVEL \_ UNRESTRICTED". Para habilitar este tipo de escenario, deben implementarse las excepciones de firewall que se detallan en este documento.

Las siguientes configuraciones de firewall son necesarias para garantizar una interoperabilidad fluida entre un firewall y Teredo:

-   El firewall de cliente debe permitir la resolución de teredo.ipv6.microsoft.com.
-   El puerto UDP 3544 debe estar abierto para asegurarse de que los clientes de Teredo puedan comunicarse correctamente con el servidor de Teredo.
-   El firewall debe recuperar los puertos UDP dinámicos que usa el servicio Teredo en el equipo local mediante una llamada a la [**función FwpmSystemPortsGet0.**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) los puertos pertinentes son de tipo FWPM \_ SYSTEM \_ PORT \_ TEREDO. La **función FwpmSystemPortsGet0** debe implementarse en lugar de las funciones [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) o [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) ahora en desuso.
-   El firewall permite que el sistema envíe y reciba paquetes UDP/IPv4 al puerto UDP 1900 en la subred local, ya que esto permite que fluya el tráfico de detección de UPnP y tenga el potencial de mejorar las tasas de conectividad.
    > [!Note]  
    > Si no se cumple esta condición, se introduce la posibilidad de que los escenarios encuentren problemas de compatibilidad relacionados con la comunicación entre determinados tipos NAT. específicamente entre los NAT simétricos y los NAT restringidos. Aunque los NAT simétricos son populares en zonas activas y los NAT restringidos son populares en los hogar, la comunicación entre los dos tiene el potencial de error en el lado de la NAT restringida.

     

-   Las excepciones "Solicitud de eco" y "Respuesta de eco" ICMPv6 entrantes y salientes deben estar habilitadas. Estas excepciones son necesarias para asegurarse de que un cliente de Teredo puede actuar como una retransmisión específica del host de Teredo. Una retransmisión específica del host de Teredo se puede identificar mediante la dirección IPv6 nativa adicional o una dirección 6to4 proporcionada con la dirección teredo.

Los firewalls de cliente deben admitir las siguientes funciones de detección y mensajes de error ICMPv6 según RFC 4443:



| Código    | Descripción                                    |
|---------|------------------------------------------------|
| 135/136 | Anuncio y solicitud de vecino ICMPV6 |
| 133/134 | Anuncio y solicitud de enrutador          |
| 128/129 | Solicitud y respuesta de eco ICMPV6                  |
| 1       | Destino no accesible                        |
| 2       | Paquete demasiado grande                               |
| 3       | Tiempo superado                                  |
| 4       | Parámetro no válido                              |



 

Si estos mensajes no se pueden permitir específicamente, se debe habilitar la exención de todos los mensajes ICMPv6 en el firewall. Además, el firewall del host puede observar que los paquetes clasificados por los códigos 135/136 o 133/134 proceden del servicio en modo de usuario **iphlpsvc** o no de la pila. El firewall del host no debe descartar estos paquetes. El servicio Teredo se implementa principalmente dentro del servicio del asistente de IP "modo de usuario".

Mediante la API de firewall de Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) para enumerar todas las reglas con la marca Edge Traversal establecida, todas las aplicaciones que quieran escuchar el tráfico no solicitado se enumeran para la excepción del firewall. La información específica sobre el uso de la opción Edge Traversal se detalla en Recepción de tráfico no solicitado [a través de Teredo.](receiving-unsolicited-traffic-over-teredo.md)

Las devoluciones de llamada no están asociadas al siguiente código de enumeración de ejemplo; Se recomienda encarecidamente que los firewalls de terceros realicen la enumeración periódicamente, o siempre que el firewall detecte una nueva aplicación que intente pasar por el firewall.


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



 

 