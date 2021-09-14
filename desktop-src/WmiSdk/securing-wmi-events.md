---
description: El proveedor de eventos entrega los eventos WMI a un consumidor temporal o permanente. El sistema de eventos WMI usa la comparación de descriptores de seguridad en eventos y SID de cuentas de usuario para controlar el acceso a eventos.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Protección de eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967135"
---
# <a name="securing-wmi-events"></a>Protección de eventos WMI

El proveedor de [](gloss-e.md) eventos entrega los eventos WMI a un [*consumidor temporal*](gloss-t.md) [*o*](gloss-p.md) permanente. El sistema de eventos WMI usa la comparación de [*descriptores*](gloss-s.md) de seguridad en eventos y [*SID*](gloss-s.md) de cuentas de usuario para controlar el acceso a eventos.

Los eventos se entregan en forma de una instancia de una clase de eventos normalmente, pero no necesariamente, derivados en última instancia de [**\_ \_ Event**](--event.md). WMI proporciona varias clases de eventos generales en las [clases del sistema WMI,](wmi-system-classes.md)como [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md). Los proveedores también pueden proporcionar sus propias clases de eventos. Por ejemplo, el proveedor [del Registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) tiene clases de eventos que informan del cambio de una clave o un valor del Registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

En los temas siguientes se proporciona información sobre cómo proteger la entrega de eventos para proveedores y la recepción de eventos de forma segura para scripts y aplicaciones cliente:

-   [Proporcionar eventos de forma segura](providing-events-securely.md)
-   [Recepción de eventos de forma segura](receiving-events-securely.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
