---
description: Los requisitos de seguridad de nivel C2 especifican que los administradores del sistema deben poder auditar los eventos relacionados con la seguridad y que el acceso a estos datos de auditoría debe limitarse a los administradores autorizados.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generación de auditoría
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073713"
---
# <a name="audit-generation"></a>Generación de auditoría

Los requisitos de seguridad de nivel C2 especifican que los administradores del sistema deben poder auditar los eventos relacionados con la seguridad y que el acceso a estos datos de auditoría debe limitarse a los administradores autorizados. La API Windows proporciona funciones que permiten a un administrador supervisar eventos relacionados con la seguridad.

El descriptor de seguridad de un objeto protegible puede tener una [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) del sistema (SACL). Una SACL contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) que especifican los tipos de intentos de acceso que generan informes de auditoría. Cada ACE identifica un administrador de confianza, un conjunto de derechos de acceso y un conjunto de marcas que indican si el sistema genera mensajes de auditoría para intentos de acceso con errores, intentos de acceso correctos o ambos.

El sistema escribe mensajes de auditoría en el registro de eventos de seguridad. Para obtener información sobre el acceso a los registros de un registro de eventos de seguridad, vea [Registro de eventos](/windows/desktop/EventLog/event-logging).

Para leer o escribir la SACL de un objeto, un subproceso debe habilitar primero el SE \_ SECURITY \_ NAME. Para obtener más información, vea [SACL Access Right](sacl-access-right.md).

La API Windows también proporciona compatibilidad para que las aplicaciones de servidor generen mensajes de auditoría cuando un cliente intenta acceder a un objeto privado. Para obtener más información, vea [Auditing Access To Private Objects](auditing-access-to-private-objects.md).

 

 
