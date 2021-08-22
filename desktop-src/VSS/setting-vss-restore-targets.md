---
description: La interfaz IVssComponent permite a un sistema de escritura ajustar exactamente cómo se restauran los archivos componente a componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Establecer destinos de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9378fe8175970a8ccacb196414f3afafbcd583ad74f9aca438a3e9b6cf6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394195"
---
# <a name="setting-vss-restore-targets"></a>Establecer destinos de restauración de VSS

La [**interfaz IVssComponent permite**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) a un sistema de escritura ajustar exactamente cómo se restauran los archivos componente a componente.

Dado que es posible que la configuración del sistema durante la restauración sea diferente de la prevista durante la copia de seguridad, se proporciona el mecanismo de destino de restauración.

Permite a los escritores llamar a [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) para cambiar cómo se restauran los componentes que se incluyen explícitamente en el documento componentes de copia de seguridad. [](vssgloss-e.md) Esto también cambia el mecanismo de restauración utilizado en los componentes que [*se incluyen implícitamente.*](vssgloss-i.md)

La restauración de archivos que tiene lugar durante un reinicio del sistema (en los valores de enumeración [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS RME RESTORE AT REBOOT y \_ \_ \_ \_ VSS \_ RME RESTORE AT REBOOT IF CANNOT REPLACE) \_ \_ no \_ \_ \_ \_  puede verse afectada por los destinos de restauración porque no hay ningún servicio VSS en ejecución cuando MoveFileEx copia archivos en su ubicación final.

De forma similar, las restauraciones personalizadas de VSS RME pueden verse afectadas o no, ya que cada restauración personalizada es específica de un escritor determinado y puede optar por respetar o omitir los \_ \_ destinos de restauración.

Los solicitantes y escritores pueden usar [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para comprobar el destino de restauración de un conjunto de componentes.

[**IVssComponent admite**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) los siguientes destinos de restauración, que se pueden establecer en un componente establecido por conjunto de componentes:

-   VSS \_ RT \_ ORIGINAL. Se respetará el método de restauración especificado por la enumeración [**\_ \_ ENUM DE VSS RESTOREMETHOD.**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)
-   VSS \_ RT \_ ALTERNATE. Los archivos se restauran en una ubicación determinada a partir de una asignación de ubicación alternativa existente. Si existe una asignación de ubicación alternativa que coincida con una ruta de acceso en un subcomponente del conjunto de componentes, restaure a la ubicación alternativa si es posible; de lo contrario, devuelva un error.

 

 



