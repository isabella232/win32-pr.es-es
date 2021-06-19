---
description: Usa seguridad de nivel de transporte del protocolo de autenticación extensible (EAP-TLS) con certificados para autenticarse en la red (WPA2-Enterprise).
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: WPA2-Enterprise ejemplo de perfil TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba561f552614896ca5da1522180a53146dc5ce54
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394830"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a><span data-ttu-id="0a334-103">WPA2-Enterprise ejemplo de perfil TLS</span><span class="sxs-lookup"><span data-stu-id="0a334-103">WPA2-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="0a334-104">Este perfil de ejemplo usa seguridad de nivel de transporte del protocolo de autenticación extensible (EAP-TLS) con certificados para autenticarse en la red.</span><span class="sxs-lookup"><span data-stu-id="0a334-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="0a334-105">Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo Enterprise (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="0a334-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="0a334-106">El WPA2-Enterprise de seguridad usa 802.1X para el intercambio de autenticación con el back-end.</span><span class="sxs-lookup"><span data-stu-id="0a334-106">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="0a334-107">El Estándar de cifrado avanzado cifrado (AES) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="0a334-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="0a334-108">Las credenciales EAP-TLS se obtienen del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="0a334-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="0a334-109">Si se produce un error en la autenticación basada en las credenciales del almacén de certificados, se solicita al usuario que proporcione credenciales válidas.</span><span class="sxs-lookup"><span data-stu-id="0a334-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="0a334-110">No se usan servidores alternativos, entidad de certificación raíz ni nombres de usuario para la autenticación si se produce un error en el primer intento.</span><span class="sxs-lookup"><span data-stu-id="0a334-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="0a334-111">La configuración de EAPHost usada en este ejemplo de perfil inalámbrico se deriva del ejemplo de propiedades de conexión [EAP-TLS.](../eaphost/eap-tls-connection-properties.md)</span><span class="sxs-lookup"><span data-stu-id="0a334-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="0a334-112">**Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="0a334-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="0a334-113">La configuración predeterminada de [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecido en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="0a334-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="0a334-114">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio laN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="0a334-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="0a334-115">El valor predeterminado era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a334-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="0a334-116">Consulte la descripción del [**elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0a334-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="0a334-117">**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2:** No se admite EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="0a334-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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

## <a name="related-topics"></a><span data-ttu-id="0a334-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a334-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a334-119">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="0a334-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
