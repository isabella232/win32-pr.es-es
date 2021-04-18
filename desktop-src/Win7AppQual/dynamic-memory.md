---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697737"
---
# <a name="dynamic-memory"></a>Memoria dinámica

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes (que se ejecutan como máquinas virtuales)** : Windows Vista \| Windows 7  
**Servidores** : Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : alta  






## <a name="description"></a>Descripción

En un nivel alto, Hyper-V Memoria dinámica es una mejora de la administración de memoria para el rol Hyper-V que se incluye en Windows Server 2008 R2 SP1. Está diseñado para su uso en producción y permite a los clientes lograr mayores proporciones de la consolidación o la densidad de la máquina virtual (VM) a la vez que optimiza el uso de memoria en el equipo físico. Se reduce la asignación de memoria estática y se asigna memoria adicional según sea necesario. Memoria dinámica afecta a los desarrolladores de software que desean asegurarse de que su software funciona correctamente en un entorno de máquina virtual.

## <a name="usage-scenario"></a>Escenario de uso

Hay dos escenarios de uso clave en los que Memoria dinámica entra en juego, en las aplicaciones del lado host y en las aplicaciones del lado invitado.

**Aplicaciones del lado host (herramientas de administración)**

Las herramientas antiguas que administran un nuevo servidor de Windows Server 2008 R2 SP1 no podrán tener acceso a la nueva configuración de Memoria dinámica. Se han desarrollado nuevas API y contadores de rendimiento de WMI para administrar la nueva configuración de Memoria dinámica para máquinas virtuales de Hyper-V. Los desarrolladores de software que trabajan en herramientas de administración deben aprovechar estas API y contadores para su uso con Windows Server 2008 R2 SP1 con el rol de Hyper-V instalado. Los detalles sobre estas nuevas API estarán disponibles a través [de la documentación del proveedor de WMI de Hyper-V en MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).

**Aplicaciones del invitado**

Los desarrolladores que escriben software para su uso en una máquina virtual configurada para utilizar Memoria dinámica deben tener en cuenta que la memoria del sistema de la máquina virtual ya no es constante. Por lo tanto, la aplicación debe liberar memoria cuando ya no se necesite para permitir que otras aplicaciones aprovechen el recurso.

Las asignaciones de memoria y las anulaciones de asignación continúan funcionando como es habitual en las aplicaciones de usuario. Memoria dinámica es completamente transparente para la mayoría de las aplicaciones de usuario final. Sin embargo, si el software que se está desarrollando utiliza contadores de rendimiento de memoria en la máquina virtual, se deben realizar pruebas exhaustivas en un entorno de Memoria dinámica habilitado para asegurarse de que el software realice los cambios que se realizan en la asignación de memoria del sistema operativo invitado. La memoria disponible ya no es "estática" de la perspectiva de la máquina virtual.

## <a name="solutions"></a>Soluciones

Las máquinas virtuales deben tener instalado Integration Services (SP1) para poder aprovechar las ventajas de Memoria dinámica. Asegúrese de que todas las máquinas usadas en la administración de máquinas virtuales de Hyper-V usan los bits más recientes de Windows Server 2008 R2 SP1.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Memoria dinámica que va a entrar en el blog de Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Usar el proveedor WMI de Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Declinación de responsabilidades

La información contenida en este documento se relaciona con el producto de software de versión preliminar que se puede modificar sustancialmente antes de la primera versión comercial. En consecuencia, es posible que la información no describa o refleje con precisión el producto de software cuando se lance por primera vez. Este documento es meramente informativo. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
