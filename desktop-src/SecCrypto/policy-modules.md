---
description: Los módulos de directivas son programas que reciben solicitudes de los servicios de Certificate Server, evalúan esas solicitudes y especifican propiedades opcionales de los certificados compilados para rellenar estas solicitudes.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Módulos de directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002849"
---
# <a name="policy-modules"></a>Módulos de directivas

Los módulos de directivas son programas que reciben solicitudes de los servicios de Certificate Server, evalúan esas solicitudes y especifican propiedades opcionales de los certificados compilados para rellenar estas solicitudes. Un módulo de directivas se implementa como una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll). Un módulo de directivas puede usar la interfaz [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para comunicarse con los servicios de Certificate Server. Los servicios de Certificate Server se comunican con un módulo de directivas mediante llamadas COM directas o, si el módulo no admite llamadas COM directas, por medio de la automatización.

Un módulo de directivas puede ver las propiedades y extensiones de certificado existentes y también puede ver los atributos y las propiedades de la solicitud. Además, un módulo de directivas puede configurar o modificar las extensiones de certificado y las propiedades "NotBefore" y "noolaetaer", así como el [*nombre distintivo relativo*](../secgloss/r-gly.md) (RDN) de un sujeto del certificado, sujeto a ciertas restricciones. En última instancia, un módulo de directivas emite o deniega la [*solicitud de certificado*](../secgloss/c-gly.md) o la mantiene pendiente.

Antes de escribir un módulo de directivas personalizado, considere la posibilidad de usar uno de los módulos de directivas predeterminados. Tanto la entidad de [*certificación*](../secgloss/c-gly.md) (CA) empresarial de servicios de servidor de certificados como la CA independiente se suministran con un módulo de directivas predeterminado adecuado. Los módulos de directivas predeterminados Enterprise e independiente emiten solicitudes de certificado (aunque la directiva predeterminada independiente debe contener el certificado pendiente hasta que un administrador lo emita manualmente). Una entidad de certificación empresarial solo debe usar el módulo de directivas empresariales proporcionado por Microsoft.

La CA empresarial requiere Active Directory. Entre las características adicionales de su módulo de directivas predeterminado se incluyen plantillas de certificado, seguridad de la [*lista de control de acceso*](../secgloss/a-gly.md) (ACL) en las plantillas de certificado para asegurarse de que las solicitudes se emiten solo para las extensiones predefinidas autorizadas que se agreguen al certificado emitido y admitan certificados de inicio de sesión de dominio de tarjeta inteligente.

El módulo de directiva de CA independiente predeterminado no es compatible con muchas de las características del módulo Enterprise predeterminado, pero admite la emisión de certificados de tarjeta inteligente. Para obtener detalles específicos, así como las funcionalidades más recientes del módulo de directivas predeterminado, consulte la documentación del producto.

En el caso de las instalaciones en las que el módulo de directivas predeterminado es inaceptable, los servicios de Certificate Server permiten módulos de directivas personalizados. Para obtener más información, consulte [escribir módulos de directivas personalizados](writing-custom-modules.md).

 

 
