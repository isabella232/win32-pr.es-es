---
description: Se usa para autenticarse en una red inalámbrica por primera vez antes de que el equipo se haya unido a un dominio.
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: Ejemplo de Perfil de bootstrap
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96c7daa6bdc72146400973d08c9e5780092b214a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277358"
---
# <a name="bootstrap-profile-sample"></a><span data-ttu-id="5629e-103">Ejemplo de Perfil de bootstrap</span><span class="sxs-lookup"><span data-stu-id="5629e-103">Bootstrap Profile Sample</span></span>

<span data-ttu-id="5629e-104">El ejemplo de Perfil de arranque se puede usar para autenticarse en una red inalámbrica por primera vez antes de que el equipo se haya unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5629e-104">The Bootstrap profile sample can be used to authenticate to a wireless network for the first time before the computer has joined a domain.</span></span>

<span data-ttu-id="5629e-105">Este perfil no valida los certificados presentados por el servidor de Servicio de autenticación remota telefónica de usuario (RADIUS) y no debe usarse después de que el equipo se haya unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5629e-105">This profile does not validate the certificates presented by the Remote Authentication Dial-In User Service (RADIUS) server, and should not be used after the machine is joined to a domain.</span></span>

<span data-ttu-id="5629e-106">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo de empresa (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="5629e-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="5629e-107">Se pueden usar otros tipos de seguridad siempre que el método de autenticación sea PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="5629e-107">Other security types can be used as long as the authentication method is PEAP-MSCHAPv2.</span></span>

<span data-ttu-id="5629e-108">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="5629e-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="5629e-109">La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5629e-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="5629e-110">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="5629e-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="5629e-111">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5629e-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5629e-112">Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5629e-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="5629e-113">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5629e-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="5629e-114">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5629e-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="5629e-115">Los elementos secundarios [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md)y [**singleSignOn**](onexschema-singlesignon-onex-element.md) del elemento [**Onex**](onexschema-onex-element.md) no se admiten y deben quitarse del perfil antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="5629e-115">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <authMode>machineOrUser</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
               <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="5629e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5629e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5629e-117">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="5629e-117">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="5629e-118">Unión de un cliente inalámbrico de Windows Vista a un dominio</span><span class="sxs-lookup"><span data-stu-id="5629e-118">Joining a Windows Vista Wireless Client to a Domain</span></span>](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



