---
description: Los módulos de salida reciben notificaciones del motor de servidor cuando se producen operaciones como la emisión de un certificado.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Módulos de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277957"
---
# <a name="exit-modules"></a>Módulos de salida

Los módulos de salida reciben notificaciones del motor de servidor cuando se producen operaciones como la emisión de un certificado. Un módulo de salida se implementa como una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll). Una operación típica para un módulo de salida es publicar un certificado completado en una ubicación especificada (el módulo de salida de la entidad de certificación empresarial predeterminada, por ejemplo, publica certificados de usuario y [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) en el Active Directory). Un módulo de salida puede usar la interfaz [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) para comunicarse con los servicios de Certificate Server. Los servicios de Certificate Server se comunican con un módulo de salida por medio de llamadas COM directas o, si el módulo no admite llamadas COM directas, por medio de la automatización.

Un módulo de salida puede ver las propiedades y extensiones de certificado existentes y también puede ver los atributos y las propiedades de la solicitud. Sin embargo, un módulo de salida no puede modificar ninguna propiedad.

Los servicios de Certificate Server proporcionan un módulo de salida predeterminado, pero también puede crear módulos de salida personalizados para satisfacer las necesidades especiales. Sin embargo, antes de escribir un módulo de salida personalizado, considere la posibilidad de usar el módulo de salida predeterminado. Además, para una entidad de certificación empresarial, siempre se debe usar el módulo de salida predeterminado, aunque se pueden agregar módulos de salida personalizados adicionales. Para obtener más información, consulte [escribir módulos de salida personalizados](writing-custom-exit-modules.md).

 

 
