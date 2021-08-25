---
description: La interfaz IX509SCEPEnrollment expone los métodos siguientes.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993545"
---
# <a name="ix509scepenrollment-methods"></a>Métodos IX509SCEPEnrollment

La [**interfaz IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expone los métodos siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                              | Descripción                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Cree un mensaje de solicitud PKCS10 con una contraseña de desafío. El mensaje de solicitud está en un PKCS7 sobre cifrado con el certificado de cifrado de servidor SCEP y firmado por el certificado de firma de servidor.<br/> |
| [**Método CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recuperar un certificado emitido previamente.<br/>                                                                                                                                                                   |
| [**Método CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Cree un mensaje para el sondeo de certificados (inscripción manual).<br/>                                                                                                                                               |
| [**Método DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Elimine los certificados o claves creados para la solicitud.<br/>                                                                                                                                                    |
| [**Inicializar método**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inicialice la instancia como preparación para una nueva solicitud.<br/>                                                                                                                                                   |
| [**Método InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inicialice la instancia de para prepararse para generar un mensaje para recuperar un certificado emitido o instalar una respuesta para una solicitud anterior por parte del emisor.<br/>                                              |
| [**Método ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Procese un mensaje de respuesta y devuelva la disposición del mensaje.<br/>                                                                                                                                       |



 

 

 




