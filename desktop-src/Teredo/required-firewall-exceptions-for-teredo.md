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
# <a name="required-firewall-exceptions-for-teredo"></a>Excepciones de Firewall necesarias para Teredo

Para que una aplicación reciba tráfico Teredo, la aplicación debe tener permiso para recibir tráfico IPv6 en el firewall del host y la aplicación debe establecer la opción de socket [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) en "nivel de protección no \_ \_ restringido". Para habilitar este tipo de escenario, se deben implementar las excepciones de firewall que se detallan en este documento.

Las siguientes configuraciones de firewall son necesarias para garantizar una interoperación fluida entre un firewall y Teredo:

-   El firewall del cliente debe permitir la resolución de teredo.ipv6.microsoft.com.
-   El puerto UDP 3544 debe estar abierto para asegurarse de que los clientes Teredo puedan comunicarse correctamente con el servidor Teredo.
-   El Firewall debe recuperar los puertos UDP dinámicos usados por el servicio Teredo en el equipo local llamando a la función [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . los puertos pertinentes son del tipo FWPM \_ del sistema \_ \_ Teredo. La función **FwpmSystemPortsGet0** debe implementarse en lugar de las funciones [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) o [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) en desuso.
-   El Firewall permite al sistema enviar y recibir paquetes UDP/IPv4 al puerto UDP 1900 en la subred local, ya que esto permite que el tráfico de detección de UPnP fluya y tenga el potencial de mejorar las tasas de conectividad.
    > [!Note]  
    > Si no se cumple esta condición, se introduce la posibilidad de que se produzcan problemas de compatibilidad que impliquen la comunicación entre determinados tipos de NAT; específicamente entre NAT simétricos y NAT restringidos. Aunque los NAT simétricos son populares en las zonas activas y los NAT restringidos son populares en casa, la comunicación entre los dos tiene la posibilidad de que se produzca un error en el lado de la NAT restringida.

     

-   Las excepciones ICMPv6 entrante y saliente "solicitud de Eco" y "respuesta de Eco" deben estar habilitadas. Estas excepciones son necesarias para garantizar que un cliente Teredo pueda actuar como una retransmisión específica del host Teredo. Una retransmisión específica del host Teredo se puede identificar mediante la dirección IPv6 nativa adicional o una dirección 6to4 suministrada con la dirección Teredo.

Los firewalls de cliente deben admitir los siguientes mensajes de error de ICMPv6 y funciones de detección por RFC 4443:



| Código    | Descripción                                    |
|---------|------------------------------------------------|
| 135/136 | Aviso y solicitud de vecino ICMPV6 |
| 133/134 | Solicitud y anuncio de enrutador          |
| 128/129 | Solicitud de eco ICMPV6 y respuesta                  |
| 1       | Destino no accesible                        |
| 2       | Paquete demasiado grande                               |
| 3       | Tiempo superado                                  |
| 4       | Parámetro no válido                              |



 

Si estos mensajes no se pueden permitir específicamente, la exención de todos los mensajes ICMPv6 debe estar habilitada en el firewall. Además, es posible que el firewall del host Observe que los paquetes clasificados por los códigos 135/136 o 133/134 proceden del servicio de modo de usuario **Iphlpsvc** y no de la pila. El firewall del host no debe quitar estos paquetes. El servicio Teredo se implementa principalmente en el servicio auxiliar IP "modo de usuario".

Con la API de Firewall de Windows de [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) para enumerar todas las reglas con la marca de cruce seguro del perímetro, todas las aplicaciones que desean escuchar el tráfico no solicitado se enumeran para la excepción de Firewall. La información específica sobre el uso de la opción de cruce seguro del perímetro se detalla en [recibir tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md).

Las devoluciones de llamada no están asociadas al código de enumeración de ejemplo siguiente; se recomienda encarecidamente que los firewalls de terceros realicen la enumeración periódicamente, o siempre que el Firewall detecte una nueva aplicación que intente pasar por el firewall.


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



 

 