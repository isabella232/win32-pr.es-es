---
description: Se usa para escenarios que requieren la autenticación de 802.1 X antes del inicio de sesión de Windows.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Ejemplo de Perfil de un solo Sign-On
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 077ed95095150e81ad9a3d7412d1940dcb1b33e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678459"
---
# <a name="single-sign-on-profile-sample"></a><span data-ttu-id="8ccb3-103">Ejemplo de Perfil de un solo Sign-On</span><span class="sxs-lookup"><span data-stu-id="8ccb3-103">Single Sign-On Profile Sample</span></span>

<span data-ttu-id="8ccb3-104">El ejemplo de Perfil de inicio de sesión único (SSO) se puede usar para escenarios que requieren la autenticación 802.1 X antes del inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-104">The single sign-on (SSO) profile sample can be used for scenarios that require 802.1X authentication before Windows logon.</span></span>

<span data-ttu-id="8ccb3-105">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo de empresa (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="8ccb3-106">El protocolo de autenticación extensible protegido con el protocolo de autenticación por desafío mutuo de Microsoft versión 2 (PEAP-MSCHAPv2) se usa para la autenticación de red.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-106">Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) is used for network authentication.</span></span> <span data-ttu-id="8ccb3-107">Las credenciales de inicio de sesión de Windows se usan para la autenticación PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-107">The Windows logon credentials are used for PEAP-MSCHAPv2 authentication.</span></span>

<span data-ttu-id="8ccb3-108">Aunque este ejemplo está configurado para usar WPA2-Enterprise y PEAP-MSCHAPv2, los perfiles de SSO se pueden configurar con otros tipos de autenticación y seguridad.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-108">While this sample is configured to use WPA2-Enterprise and PEAP-MSCHAPv2, SSO profiles can be configured with other security and authentication types.</span></span>

<span data-ttu-id="8ccb3-109">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="8ccb3-110">La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="8ccb3-111">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="8ccb3-112">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="8ccb3-113">Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ccb3-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="8ccb3-114">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ccb3-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="8ccb3-115">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ccb3-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="8ccb3-116">Los elementos secundarios [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**AuthMode**](onexschema-authmode-onex-element.md)y [**singleSignOn**](onexschema-singlesignon-onex-element.md) del elemento [**Onex**](onexschema-onex-element.md) no se admiten y deben quitarse del perfil antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-116">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
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
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
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
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="8ccb3-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ccb3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ccb3-118">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="8ccb3-118">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



