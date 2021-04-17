---
description: La interfaz IVssComponent permite a un escritor ajustar exactamente cómo se restauran los archivos componente por componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Establecimiento de destinos de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696968"
---
# <a name="setting-vss-restore-targets"></a>Establecimiento de destinos de restauración de VSS

La interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite a un escritor ajustar exactamente cómo se restauran los archivos componente por componente.

Dado que es posible que la configuración del sistema durante la restauración no sea la esperada durante la copia de seguridad, se proporciona el mecanismo de destino de la restauración.

Permite a los escritores llamar a [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) para cambiar el modo en que se restauran los componentes que se [*incluyen explícitamente*](vssgloss-e.md) en el documento de componentes de copia de seguridad. Esto también cambia el mecanismo de restauración usado en los componentes que se incluyen de forma [*implícita*](vssgloss-i.md).

La restauración de archivos que tiene lugar durante un reinicio del sistema (bajo los valores de enumeración de RESTOREMETHOD de la enumeración de la enumeración [**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) de VSS la \_ \_ restauración \_ de RME al \_ reiniciar y VSS \_ RME \_ restore \_ en el \_ reinicio \_ si \_ no se puede \_ reemplazar) no puede verse afectado por los destinos de restauración porque no hay ningún servicio VSS en ejecución cuando **MoveFileEx** copia los archivos en su ubicación

Del mismo modo, las \_ restauraciones personalizadas de RME de VSS \_ pueden verse afectadas o no, ya que cada restauración personalizada es específica de un escritor determinado y puede decidir o omitir los destinos de restauración.

Los solicitantes y escritores pueden usar [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para comprobar el destino de restauración de un conjunto de componentes.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) admite los siguientes destinos de restauración, que se pueden establecer en un componente establecido por el conjunto de componentes:

-   VSS \_ RT \_ original. Se respetará el método restore especificado por la enumeración de enumeración [**\_ \_ RESTOREMETHOD de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) .
-   VSS \_ RT \_ alternativo. Los archivos se restauran en una ubicación determinada a partir de una asignación de ubicación alternativa existente. Si existe una asignación de ubicación alternativa que coincide con una ruta de acceso en un subcomponente de conjunto de componentes, restaure a la ubicación alternativa si es posible; de lo contrario, devuelve un error.

 

 



