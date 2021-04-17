---
description: La API de inscripción de certificados admite las siguientes interfaces de uso general.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688279"
---
# <a name="helper-interfaces"></a>Interfaces auxiliares

La API de inscripción de certificados admite las siguientes interfaces de uso general.



| Interfaz                                                                    | Descripción                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | Crea una cadena con codificación Unicode a partir de una matriz de bytes, crea una matriz de bytes a partir de una cadena codificada con Unicode y modifica el tipo de codificación Unicode que se aplica a una cadena. |
| [**ICertificateAttestationChallenge**](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | Admite los desafíos de atestación de certificados.                                                                                                                           |
| [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | Representa un identificador de objeto.                                                                                                                                       |
| [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | Administra una colección de objetos [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .                                                                                                        |
| [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | Representa un nombre distintivo X. 500.                                                                                                                                |
| [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | Interfaz de clave de aprobación X. 509                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



