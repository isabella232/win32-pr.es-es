---
description: La interfaz IOCSPAdmin define los métodos siguientes. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de IOCSPAdmin, consulte Propiedades de IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Métodos de IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a455ae5cfbb49d60cc0d0a03265d05c98efa2f2217746086b0acf0a4230709dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992855"
---
# <a name="methods-of-iocspadmin"></a>Métodos de IOCSPAdmin

La interfaz [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) define los métodos siguientes. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **IOCSPAdmin**, vea [Propiedades de IOCSPAdmin](properties-of-iocspadmin.md).



| Método                                                              | Descripción                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Se conecta a un servidor respondedor del Protocolo de estado de certificado en línea (OCSP) e inicializa un objeto **OCSPAdmin** con la información de configuración del servidor.                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Obtiene una lista de nombres de algoritmo hash. El servidor respondedor usa uno de los algoritmos con nombre para firmar respuestas OCSP para una configuración de entidad de [*certificación*](../secgloss/c-gly.md) (CA) determinada. |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Obtiene la máscara de acceso de roles de privilegios para un usuario en un servidor de respondedor determinado.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Obtiene información del descriptor de seguridad para un servidor de respondedor.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Obtiene los certificados de firma que están disponibles en un servidor de respondedor para un certificado de entidad de certificación determinado.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Prueba una conexión DCOM con un servicio de respondedor.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Actualiza un servicio de respondedor con cambios de configuración.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Actualiza la información del descriptor de seguridad para un servidor respondedor OCSP.                                                                                                                                                                                                     |



 

 

 
