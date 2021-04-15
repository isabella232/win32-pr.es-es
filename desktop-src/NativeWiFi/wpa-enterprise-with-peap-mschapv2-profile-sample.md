---
description: Usa el protocolo de autenticación extensible protegido con el protocolo de autenticación por desafío mutuo de Microsoft versión 2 (PEAP-MSCHAPv2) con el nombre de usuario y la contraseña para autenticarse en la red.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: WPA-Enterprise con PEAP-MSCHAPv2 ejemplo de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787cc2e4652d3b588b49faf2f9215cd9bd1936e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498017"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="419a8-103">WPA-Enterprise con PEAP-MSCHAPv2 ejemplo de perfil</span><span class="sxs-lookup"><span data-stu-id="419a8-103">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="419a8-104">Este perfil de ejemplo usa el protocolo de autenticación extensible protegido con el protocolo de autenticación por desafío mutuo de Microsoft versión 2 (PEAP-MSCHAPv2) con contraseña \* UserName \* **/**  para autenticarse en la red.</span><span class="sxs-lookup"><span data-stu-id="419a8-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="419a8-105">Se solicita al usuario que escriba las credenciales.</span><span class="sxs-lookup"><span data-stu-id="419a8-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="419a8-106">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo de empresa (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="419a8-106">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="419a8-107">El tipo de seguridad WPA-Enterprise usa 802.1 X para el intercambio de autenticación con el back-end.</span><span class="sxs-lookup"><span data-stu-id="419a8-107">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="419a8-108">El protocolo de integridad de clave temporal (TKIP) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="419a8-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="419a8-109">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="419a8-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="419a8-110">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="419a8-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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

## <a name="related-topics"></a><span data-ttu-id="419a8-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="419a8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419a8-112">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="419a8-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



