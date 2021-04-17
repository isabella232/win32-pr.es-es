---
description: Se usa para conectarse a una red que usa el protocolo de autenticación extensible protegido con el protocolo de autenticación por desafío mutuo de Microsoft versión 2 (PEAP-MSCHAPv2) con el nombre de usuario y la contraseña para la autenticación de 802.1 X.
ms.assetid: b5dde0d0-940f-40ec-b24d-95a76325ff1b
title: Ejemplo de perfil PEAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db34a3a99305f3506e3b34fde48f41e5a4c72ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677747"
---
# <a name="peap-profile-sample"></a><span data-ttu-id="eb5bf-103">Ejemplo de perfil PEAP</span><span class="sxs-lookup"><span data-stu-id="eb5bf-103">PEAP Profile Sample</span></span>

<span data-ttu-id="eb5bf-104">Este ejemplo de perfil muestra un perfil de red cableada que se usa para conectarse a una red que usa el protocolo de autenticación extensible protegido con el protocolo de autenticación por desafío mutuo de Microsoft versión 2 (PEAP-MSCHAPv2) con la contraseña \* UserName \* **/**  para la autenticación de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-104">This profile sample shows a wired network profile used to connect to a network that uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ for 802.1X authentication.</span></span> <span data-ttu-id="eb5bf-105">Se solicita al usuario que escriba las credenciales.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-105">The user is prompted to enter credentials.</span></span>

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
</LANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="eb5bf-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb5bf-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb5bf-107">Ejemplos de perfil con cable</span><span class="sxs-lookup"><span data-stu-id="eb5bf-107">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 



