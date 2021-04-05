---
description: Usa seguridad de nivel de transporte (EAP-TLS) del Protocolo de autenticación extensible con certificados para autenticarse en la red.
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise con el ejemplo de perfil TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002768"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="1e728-103">WPA-Enterprise con el ejemplo de perfil TLS</span><span class="sxs-lookup"><span data-stu-id="1e728-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="1e728-104">Este perfil de ejemplo usa seguridad de nivel de transporte (EAP-TLS) del Protocolo de autenticación extensible con certificados para autenticarse en la red.</span><span class="sxs-lookup"><span data-stu-id="1e728-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="1e728-105">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo de empresa (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="1e728-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="1e728-106">El tipo de seguridad WPA-Enterprise usa 802.1 X para el intercambio de autenticación con el back-end.</span><span class="sxs-lookup"><span data-stu-id="1e728-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="1e728-107">El protocolo de integridad de clave temporal (TKIP) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="1e728-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="1e728-108">Las credenciales de EAP-TLS se obtienen del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="1e728-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="1e728-109">Si se produce un error en la autenticación basada en las credenciales del almacén de certificados, se solicitará al usuario que proporcione credenciales válidas.</span><span class="sxs-lookup"><span data-stu-id="1e728-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="1e728-110">No se usan servidores alternativos, entidades de certificación raíz o nombres de usuario para la autenticación si se produce un error en el primer intento.</span><span class="sxs-lookup"><span data-stu-id="1e728-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="1e728-111">La configuración de EAPHost usada en este ejemplo de perfil inalámbrico se deriva del ejemplo de [propiedades de conexión EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="1e728-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="1e728-112">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="1e728-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="1e728-113">La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1e728-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="1e728-114">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="1e728-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="1e728-115">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e728-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="1e728-116">Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1e728-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="1e728-117">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** EAP-TLS no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1e728-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
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
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="1e728-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e728-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e728-119">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="1e728-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
