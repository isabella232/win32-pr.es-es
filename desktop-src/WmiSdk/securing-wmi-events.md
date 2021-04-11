---
description: El proveedor de eventos entrega los eventos WMI a un consumidor temporal o permanente. El sistema de eventos WMI utiliza la comparación de descriptores de seguridad en los eventos y SID de la cuenta de usuario para controlar el acceso a los eventos.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Proteger eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276133"
---
# <a name="securing-wmi-events"></a>Proteger eventos WMI

El [*proveedor de eventos*](gloss-e.md) entrega los eventos WMI a un consumidor [*temporal*](gloss-t.md) o [*permanente*](gloss-p.md) . El sistema de eventos WMI utiliza la comparación de [*descriptores de seguridad*](gloss-s.md) en los eventos y [*SID*](gloss-s.md) de la cuenta de usuario para controlar el acceso a los eventos.

Los eventos se entregan en forma de una instancia de una clase de eventos normalmente, pero no necesariamente, derivadas de [**\_ \_ Event**](--event.md). WMI proporciona varias clases de eventos generales en las [clases del sistema WMI](wmi-system-classes.md), como [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md). Los proveedores también pueden proporcionar sus propias clases de eventos. Por ejemplo, el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) tiene clases de eventos que informan del cambio de una clave o un valor del registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

En los temas siguientes se proporciona información acerca de la protección de la entrega de eventos para proveedores y la recepción segura de eventos para aplicaciones y scripts de cliente:

-   [Proporcionar eventos de forma segura](providing-events-securely.md)
-   [Recepción segura de eventos](receiving-events-securely.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
