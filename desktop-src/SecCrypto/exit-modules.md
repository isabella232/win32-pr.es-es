---
description: Los módulos de salida reciben notificaciones del motor de servidor cuando se producen operaciones como la emisión de un certificado.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Salir de módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173213"
---
# <a name="exit-modules"></a>Salir de módulos

Los módulos de salida reciben notificaciones del motor de servidor cuando se producen operaciones como la emisión de un certificado. Un módulo de salida se implementa como una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (DLL). Una operación típica para un módulo de salida es publicar un certificado completado en una ubicación especificada (el módulo de salida de la entidad de certificación empresarial predeterminada, por ejemplo, publica certificados de usuario y listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) en el Active Directory). Un módulo de salida puede usar [**la interfaz ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) para comunicarse con Certificate Services. Servicios de certificados se comunica con un módulo de salida mediante llamadas COM directas o, si el módulo no admite llamadas COM directas, mediante Automation.

Un módulo de salida puede ver las propiedades y extensiones de certificado existentes, y también puede ver atributos y propiedades de solicitud. Sin embargo, un módulo de salida no puede modificar ninguna propiedad.

Servicios de certificados proporciona un módulo de salida predeterminado, pero también puede crear módulos de salida personalizados para satisfacer necesidades especiales. Sin embargo, antes de escribir un módulo de salida personalizado, considere la posibilidad de usar el módulo de salida predeterminado. Además, para una entidad de certificación empresarial, siempre se debe usar el módulo de salida predeterminado, aunque puede agregar módulos de salida personalizados adicionales. Para obtener más información, vea [Escribir módulos de salida personalizados.](writing-custom-exit-modules.md)

 

 
