---
description: La API de inscripción de certificados admite las siguientes interfaces de uso generales.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec54f9e092bb7675f18a28e7af8599a4e870b5aec1d88d0c5d3332c33c2bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779544"
---
# <a name="helper-interfaces"></a>Interfaces auxiliares

La API de inscripción de certificados admite las siguientes interfaces de uso generales.



| Interfaz                                                                    | Descripción                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | Crea una cadena codificada en Unicode a partir de una matriz de bytes, crea una matriz de bytes a partir de una cadena codificada en Unicode y modifica el tipo de codificación Unicode aplicada a una cadena. |
| [**ICertificateAttestationChallenge**](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | Admite desafíos de atestación de certificados.                                                                                                                           |
| [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | Representa un identificador de objeto.                                                                                                                                       |
| [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | Administra una colección de [**objetos IObjectId.**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                                                                                        |
| [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | Representa un nombre distintivo X.500.                                                                                                                                |
| [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | Interfaz de clave de aprobación X.509                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



