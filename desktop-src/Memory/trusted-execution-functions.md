---
description: 'Las siguientes funciones se usan al trabajar con enclaves que se usan para crear entornos de ejecución de confianza:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Funciones de ejecución de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159808"
---
# <a name="trusted-execution-functions"></a>Funciones de ejecución de confianza

Las siguientes funciones se usan al trabajar con enclaves que se usan para crear entornos de ejecución de confianza:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Llama a una función dentro de un enclave. <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Crea un nuevo enclave sin inicializar. Un enclave es una región aislada de código y datos dentro del espacio de direcciones de una aplicación. Solo el código que se ejecuta dentro del enclave puede acceder a los datos dentro del mismo enclave.<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Elimina el enclave especificado.<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Obtiene un informe de atestación de enclave que describe el enclave actual y está firmado por la autoridad responsable del tipo del enclave. <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Obtiene información sobre el enclave que se está ejecutando actualmente.<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Genera un objeto binario grande cifrado (blob) a partir de datos no administrados.<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Descifra un objeto binario grande cifrado (blob).<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Comprueba un informe de atestación que se generó en el sistema actual. <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Inicializa un enclave que creó y cargó con datos.<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Recupera si se admite el tipo de enclave especificado.<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Carga los datos en un enclave sin inicializar que creó mediante una llamada [**a CreateEnclave.**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Carga una imagen y todas sus importaciones en un enclave.<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Finaliza la ejecución de los subprocesos que se ejecutan dentro de un enclave.<br/>                                                                                                                                               |



 

 

 




