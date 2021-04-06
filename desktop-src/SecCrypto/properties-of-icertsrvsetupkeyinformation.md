---
description: La interfaz ICertSrvSetupKeyInformation define las siguientes propiedades.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propiedades de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910073"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Propiedades de ICertSrvSetupKeyInformation

La interfaz [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) define las siguientes propiedades.



| Propiedad                                                                           | Descripción                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContainerName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Obtiene o establece el nombre utilizado por el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) para generar, almacenar o tener acceso a la clave.                                                                       |
| [**Existing**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Obtiene o establece un valor que indica si la clave privada ya existe.                                                                                                                                                                                                                       |
| [**ExistingCACertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Obtiene o establece el valor binario que se ha codificado mediante [*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) y que es el valor binario del certificado de entidad de certificación que corresponde a una clave existente. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Obtiene o establece el nombre del algoritmo hash que se usa para firmar o comprobar el certificado de la entidad de certificación para la clave.                                                                                                                                                                                                |
| [**Length**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Obtiene o establece la intensidad de la clave a uno de los valores admitidos por el CSP.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Obtiene o establece el nombre del CSP que se usa para generar o almacenar la clave privada.                                                                                                                                                                                                               |



 

 

 
