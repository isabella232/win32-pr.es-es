---
description: 'Las siguientes funciones se usan cuando se trabaja con enclaves que se usan para crear entornos de ejecución de confianza:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Funciones de ejecución de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677435"
---
# <a name="trusted-execution-functions"></a>Funciones de ejecución de confianza

Las siguientes funciones se usan cuando se trabaja con enclaves que se usan para crear entornos de ejecución de confianza:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Llama a una función dentro de un enclave. <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Crea un nuevo enclave no inicializado. Un enclave es una región aislada de código y datos dentro del espacio de direcciones para una aplicación. Solo el código que se ejecuta dentro de enclave puede tener acceso a los datos del mismo enclave.<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Elimina el enclave especificado.<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Obtiene un informe de atestación de enclave que describe el enclave actual y está firmado por la autoridad responsable del tipo de enclave. <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Obtiene información sobre el enclave que se está ejecutando actualmente.<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Genera un objeto binario grande (BLOB) cifrado a partir de datos unencypted.<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Descifra un objeto binario grande (BLOB) cifrado.<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Comprueba un informe de atestación generado en el sistema actual. <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Inicializa un enclave que creó y cargó con datos.<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Recupera si se admite el tipo de enclave especificado.<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Carga datos en un enclave no inicializado que se creó mediante una llamada a [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave).<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Carga una imagen y todas sus importaciones en un enclave.<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Finaliza la ejecución de los subprocesos que se están ejecutando dentro de un enclave.<br/>                                                                                                                                               |



 

 

 




