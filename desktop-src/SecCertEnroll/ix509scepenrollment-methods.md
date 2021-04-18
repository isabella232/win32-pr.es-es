---
description: La interfaz IX509SCEPEnrollment expone los métodos siguientes.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687921"
---
# <a name="ix509scepenrollment-methods"></a>Métodos IX509SCEPEnrollment

La interfaz [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expone los métodos siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                              | Descripción                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Cree un mensaje de solicitud PKCS10 con una contraseña de desafío. El mensaje de solicitud se encuentra en un PKCS7 con doble cifrado con el certificado de cifrado del servidor SCEP y firmado por el certificado de firma del servidor.<br/> |
| [**Método CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recuperar un certificado emitido previamente.<br/>                                                                                                                                                                   |
| [**Método CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Cree un mensaje para el sondeo de certificados (inscripción manual).<br/>                                                                                                                                               |
| [**Método DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Elimine los certificados o claves creados para la solicitud.<br/>                                                                                                                                                    |
| [**Initialize (método)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inicialice la instancia como preparación para una nueva solicitud.<br/>                                                                                                                                                   |
| [**Método InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inicialice la instancia para preparar la generación de un mensaje con el fin de recuperar un certificado emitido o instalar una respuesta para una solicitud anterior del emisor.<br/>                                              |
| [**Método ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Procesa un mensaje de respuesta y devuelve la disposición del mensaje.<br/>                                                                                                                                       |



 

 

 




