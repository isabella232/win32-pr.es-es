---
description: Usa seguridad de nivel de transporte (EAP-TLS) del Protocolo de autenticación extensible con certificados para autenticarse en la red.
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: WPA2-Enterprise con el ejemplo de perfil TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd85d30bed631a55f0e7e622aac4a8ade17ba3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082141"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a>WPA2-Enterprise con el ejemplo de perfil TLS

Este perfil de ejemplo usa seguridad de nivel de transporte (EAP-TLS) del Protocolo de autenticación extensible con certificados para autenticarse en la red.

Este ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo de empresa (WPA2-Enterprise). El tipo de seguridad WPA2-Enterprise usa 802.1 X para el intercambio de autenticación con el back-end. El tipo de cifrado Estándar de cifrado avanzado (AES) se usa para el cifrado.

Las credenciales de EAP-TLS se obtienen del almacén de certificados. Si se produce un error en la autenticación basada en las credenciales del almacén de certificados, se solicitará al usuario que proporcione credenciales válidas. No se usan servidores alternativos, entidades de certificación raíz o nombres de usuario para la autenticación si se produce un error en el primer intento.

La configuración de EAPHost usada en este ejemplo de perfil inalámbrico se deriva del ejemplo de [propiedades de conexión EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas. La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado. La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado. La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista. Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** EAP-TLS no es compatible.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> </dl>

 

 
