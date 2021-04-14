---
description: La interfaz IOCSPAdmin define los siguientes métodos. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de IOCSPAdmin, consulte propiedades de IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Métodos de IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360368"
---
# <a name="methods-of-iocspadmin"></a>Métodos de IOCSPAdmin

La interfaz [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) define los siguientes métodos. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **IOCSPAdmin**, consulte [propiedades de IOCSPAdmin](properties-of-iocspadmin.md).



| Método                                                              | Descripción                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Se conecta a un servidor de respuesta del Protocolo de estado de certificados en línea (OCSP) e inicializa un objeto **OCSPAdmin** con la información de configuración del servidor.                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Obtiene una lista de nombres de algoritmo hash. El servidor de respuesta utiliza uno de los algoritmos con nombre para firmar las respuestas de OCSP para una determinada configuración de [*entidad de certificación*](../secgloss/c-gly.md) (CA). |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Obtiene la máscara de acceso de los roles de privilegio para un usuario en un servidor de respuesta determinado.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Obtiene la información del descriptor de seguridad para un servidor de respuesta.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Obtiene los certificados de firma que están disponibles en un servidor de respuesta para un certificado de CA determinado.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Prueba una conexión DCOM con un servicio de respuesta.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Actualiza un servicio Respondedor con cambios de configuración.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Actualiza la información del descriptor de seguridad de un servidor de respuesta de OCSP.                                                                                                                                                                                                     |



 

 

 
