---
description: 'Las siguientes estructuras se usan cuando se trabaja con enclaves que se usan para crear entornos de ejecución de confianza:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Estructuras de ejecución de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677689"
---
# <a name="trusted-execution-structures"></a>Estructuras de ejecución de confianza

Las siguientes estructuras se usan cuando se trabaja con enclaves que se usan para crear entornos de ejecución de confianza:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                         | Descripción                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ crear \_ información \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contiene información específica de la arquitectura que se usa para crear un enclave cuando el tipo enclave es **enclave \_ Type \_ SGX**, que especifica un enclave para la extensión de la arquitectura de las extensiones de software Guard (SGX) de Intel.<br/>     |
| [**ENCLAVE \_ Create \_ info \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contiene información específica de la arquitectura que se va a usar para crear un enclave cuando el tipo enclave es **enclave \_ Type \_ VBS**, que especifica una seguridad basada en la virtualización (vbs) enclave.<br/>                                       |
| [**identidad de ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Describe la identidad del módulo principal de un enclave. <br/>                                                                                                                                                                 |
| [**información de ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contiene información sobre el enclave que se está ejecutando actualmente.<br/>                                                                                                                                                                  |
| [**ENCLAVE \_ init \_ info \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contiene información específica de la arquitectura que se va a usar para inicializar un enclave cuando el tipo enclave es **enclave \_ Type \_ SGX**, que especifica un enclave para la extensión de la arquitectura de las extensiones de software Guard (SGX) de Intel.<br/> |
| [**ENCLAVE \_ init \_ info \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contiene información específica de la arquitectura que se va a usar para inicializar un enclave cuando el tipo enclave es **enclave \_ Type \_ VBS**, que especifica una seguridad basada en la virtualización (vbs) enclave.<br/>                                   |
| [**IMAGE \_ enclave \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Define el formato de la configuración de enclave para los sistemas que ejecutan Windows de 32 bits.<br/>                                                                                                                                          |
| [**IMAGE \_ enclave \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Define el formato de la configuración de enclave para los sistemas que ejecutan Windows de 64 bits.<br/>                                                                                                                                          |
| [**importación de IMAGE \_ enclave \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Define una entrada en la matriz de imágenes que un enclave puede importar.<br/>                                                                                                                                                           |
| [**\_Informe VBS enclave \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Describe el formato de la instrucción firmada incluida en un informe generado mediante una llamada a la función [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_módulo de \_ Informe VBS enclave \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Describe un módulo cargado para enclave.<br/>                                                                                                                                                                                   |
| [**\_encabezado de \_ paquete de informe VBS enclave \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Describe el contenido de un informe generado mediante una llamada a la función [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**VBS \_ enclave \_ \_ encabezado VARDATA de informe \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Describe el formato de un bloque de datos de variable incluido en un informe generado por la función [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
