---
description: La interfaz IX509SCEPEnrollment expone las siguientes propiedades.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Propiedades de IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687920"
---
# <a name="ix509scepenrollment-properties"></a>Propiedades de IX509SCEPEnrollment

La interfaz [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                              | Descripción                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad de certificado**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | Obtiene el certificado para la solicitud.<br/>                                                                                                       |
| [**Propiedad CertificateFriendlyName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | Obtiene o establece el nombre descriptivo del certificado.<br/>                                                                                         |
| [**Propiedad FailInfo**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | Obtiene información cuando el método [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) detecta un entorno con errores.<br/> |
| [**Propiedad OldCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | Obtiene o establece un certificado antiguo que se va a reemplazar por una solicitud.<br/>                                                                      |
| [**Propiedad request**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | Obtiene la solicitud interna de PKCS10.<br/>                                                                                                              |
| [**Propiedad ServerCapabilities**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | Establece los algoritmos hash y de cifrado preferidos para la solicitud.<br/>                                                                          |
| [**Propiedad SignerCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | Obtiene o establece el certificado del firmante para la solicitud.<br/>                                                                                        |
| [**Propiedad Silent**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | Obtiene o establece si se va a permitir la interfaz de usuario durante la solicitud.<br/>                                                                                        |
| [**Propiedad Status**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | Obtiene el estado de la solicitud.<br/>                                                                                                             |
| [**Propiedad TransactionId**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | Obtiene o establece el identificador de transacción de la solicitud.<br/>                                                                                            |



 

 

 




