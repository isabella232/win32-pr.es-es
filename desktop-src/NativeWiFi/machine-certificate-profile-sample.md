---
description: Se usa para conectarse a una red que usa certificados de seguridad de nivel de transporte del Protocolo de autenticación extensible (EAP-TLS) almacenados en el equipo local para la autenticación 802.1X.
ms.assetid: 4cc4cbb7-963f-4771-8a3d-2a37058c9011
title: Ejemplo de perfil de certificado de máquina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb76f0916f2a0d8287a5bf098983e0229c6682decbd3a72386e7b15809c27ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801105"
---
# <a name="machine-certificate-profile-sample"></a>Ejemplo de perfil de certificado de máquina

En este ejemplo de perfil se muestra un perfil de red cableada que se usa para conectarse a una red que usa certificados de seguridad de nivel de transporte del Protocolo de autenticación extensible (EAP-TLS) almacenados en el equipo local para la autenticación 802.1X. Para ver un perfil que usa certificados EAP-TLS almacenados en una tarjeta inteligente, consulte [Perfil de ejemplo de certificado de tarjeta inteligente](smart-card-certificate-profile-sample.md).

La configuración de EAPHost usada en este ejemplo de perfil inalámbrico se deriva del ejemplo de propiedades de [conexión EAP-TLS.](../eaphost/eap-tls-connection-properties.md)

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
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
</LANProfile>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de perfiles cableados](wired-profile-samples.md)
</dt> </dl>

 

 
