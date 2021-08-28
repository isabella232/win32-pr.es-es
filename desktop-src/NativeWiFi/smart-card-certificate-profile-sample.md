---
description: Se usa para conectarse a una red que usa certificados de seguridad de nivel de transporte del Protocolo de autenticación extensible (EAP-TLS) almacenados en una tarjeta inteligente para la autenticación 802.1X.
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: Ejemplo de perfil de certificado de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f609c2761c4387804f9220d5fcdcba83a05851fa8cad2e696e7f2285e0be32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984833"
---
# <a name="smart-card-certificate-profile-sample"></a>Ejemplo de perfil de certificado de tarjeta inteligente

En este ejemplo de perfil se muestra un perfil de red cableada que se usa para conectarse a una red que usa certificados de seguridad de nivel de transporte del Protocolo de autenticación extensible (EAP-TLS) almacenados en una tarjeta inteligente para la autenticación 802.1X. Para ver un perfil que usa certificados EAP-TLS almacenados en el equipo local, consulte [Ejemplo de perfil de certificado de máquina.](machine-certificate-profile-sample.md)

La configuración de EAPHost usada en este ejemplo de perfil inalámbrico se deriva del ejemplo de propiedades de conexión [EAP-TLS.](../eaphost/eap-tls-connection-properties.md)

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
                                        <eapTls:SmartCard />
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

 

 
