---
description: Usa el protocolo de autenticación extensible protegido con el protocolo de autenticación de desafío de Microsoft versión 2, con WPA-Enterprise.
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: WPA-Enterprise con el PEAP-MSCHAPv2 de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364cc7a9cc85e4c5e2ef908c0ac2a4726d6c5a96
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395050"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="e251a-103">WPA-Enterprise con el PEAP-MSCHAPv2 de perfil</span><span class="sxs-lookup"><span data-stu-id="e251a-103">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="e251a-104">Este perfil de ejemplo usa el Protocolo de autenticación extensible protegido con el protocolo de autenticación de desafío de Microsoft versión 2 (PEAP-MSCHAPv2) con la contraseña *UserName* para autenticarse en la **/**  red.</span><span class="sxs-lookup"><span data-stu-id="e251a-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="e251a-105">Se pide al usuario que escriba las credenciales.</span><span class="sxs-lookup"><span data-stu-id="e251a-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="e251a-106">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo Enterprise (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="e251a-106">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="e251a-107">El WPA-Enterprise de seguridad usa 802.1X para el intercambio de autenticación con el back-end.</span><span class="sxs-lookup"><span data-stu-id="e251a-107">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="e251a-108">El Protocolo de integridad de clave temporal (TKIP) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="e251a-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="e251a-109">**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2:** Se [**omite**](wlan-profileschema-name-wlanprofile-element.md) el elemento secundario name del elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="e251a-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="e251a-110">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del nombre [**secundario**](wlan-profileschema-name-ssid-element.md) del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)</span><span class="sxs-lookup"><span data-stu-id="e251a-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e251a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e251a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e251a-112">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="e251a-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



