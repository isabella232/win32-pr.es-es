---
description: 'Las estructuras siguientes se usan al trabajar con enclaves que se usan para crear entornos de ejecución de confianza:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Estructuras de ejecución de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386256"
---
# <a name="trusted-execution-structures"></a>Estructuras de ejecución de confianza

Las estructuras siguientes se usan al trabajar con enclaves que se usan para crear entornos de ejecución de confianza:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                         | Descripción                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ CREATE \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contiene información específica de la arquitectura que se usará para crear un enclave cuando el tipo de enclave sea **ENCLAVE \_ TYPE \_ SGX**, que especifica un enclave para la extensión de arquitectura intel Software Guard Extensions (SGX).<br/>     |
| [**ENCLAVE \_ CREATE \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contiene información específica de la arquitectura que se va a usar para crear un enclave cuando el tipo de enclave es **ENCLAVE \_ TYPE \_ VBS**, que especifica un enclave de seguridad basado en virtualización (VBS).<br/>                                       |
| [**ENCLAVE \_ IDENTITY**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Describe la identidad del módulo principal de un enclave. <br/>                                                                                                                                                                 |
| [**INFORMACIÓN \_ DE ENCLAVE**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contiene información sobre el enclave que se está ejecutando actualmente.<br/>                                                                                                                                                                  |
| [**ENCLAVE \_ INIT \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contiene información específica de la arquitectura que se va a usar para inicializar un enclave cuando el tipo de enclave es **ENCLAVE \_ TYPE \_ SGX**, que especifica un enclave para la extensión de arquitectura Intel Software Guard Extensions (SGX).<br/> |
| [**VBS \_ DE INFORMACIÓN DE ENCLAVE INIT \_ \_**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contiene información específica de la arquitectura que se usa para inicializar un enclave cuando el tipo de enclave es **ENCLAVE \_ TYPE \_ VBS**, que especifica un enclave de seguridad basado en virtualización (VBS).<br/>                                   |
| [**IMAGE \_ ENCLAVE \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Define el formato de la configuración del enclave para los sistemas que ejecutan sistemas de 32 bits Windows.<br/>                                                                                                                                          |
| [**IMAGE \_ ENCLAVE \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Define el formato de la configuración del enclave para los sistemas que ejecutan sistemas de 64 Windows.<br/>                                                                                                                                          |
| [**IMPORTACIÓN \_ DE ENCLAVE DE \_ IMAGEN**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Define una entrada en la matriz de imágenes que un enclave puede importar.<br/>                                                                                                                                                           |
| [**INFORME DE ENCLAVE DE VBS \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Describe el formato de la instrucción firmada contenida en un informe generado mediante una llamada a la [**función EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                     |
| [**MÓDULO DE INFORME \_ DE ENCLAVE \_ DE \_ VBS**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Describe un módulo cargado para el enclave.<br/>                                                                                                                                                                                   |
| [**ENCABEZADO \_ PKG DEL INFORME DE ENCLAVE \_ \_ DE \_ VBS**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Describe el contenido de un informe generado mediante una llamada a la [**función EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                                                     |
| [**ENCABEZADO \_ \_ VARDATA DEL INFORME \_ DE ENCLAVE \_ DE VBS**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Describe el formato de un bloque de datos de variable contenido en un informe que genera la [**función EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                          |



 

 

 
