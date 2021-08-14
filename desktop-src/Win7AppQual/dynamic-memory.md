---
description: Memoria dinámica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408e54aa1a1d238a98bb0eff8af2dd76862b32b77c26b3d3812d8707bc0099f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329857"
---
# <a name="dynamic-memory"></a>Memoria dinámica

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes (que se ejecutan como máquinas virtuales):** Windows Vista \| Windows 7  
**Servidores:** Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** alta  






## <a name="description"></a>Descripción

En un nivel alto, Hyper-V Memoria dinámica es una mejora de administración de memoria para el rol de Hyper-V incluido en Windows Server 2008 R2 SP1. Está diseñado para su uso en producción y permite a los clientes lograr mayores relaciones de consolidación y densidad de máquinas virtuales (VM) a la vez que optimiza el uso de memoria en la máquina física. La asignación de memoria estática se reduce y se asigna memoria adicional según sea necesario. Memoria dinámica afecta a los desarrolladores de software que desean asegurarse de que su software funciona correctamente en un entorno de máquina virtual.

## <a name="usage-scenario"></a>Escenario de uso

Hay dos escenarios de uso clave en los que Memoria dinámica en juego, las aplicaciones del lado host y las aplicaciones del lado invitado.

**Aplicaciones del lado host (herramientas de administración)**

Las herramientas antiguas que administran un nuevo servidor Windows Server 2008 R2 SP1 no podrán acceder a la nueva Memoria dinámica configuración. Se han desarrollado nuevas API WMI y contadores de rendimiento para administrar la nueva configuración de Memoria dinámica para máquinas virtuales de Hyper-V. Los desarrolladores de software que trabajan en herramientas de administración deben aprovechar estas API y contadores para su uso con Windows Server 2008 R2 SP1 con el rol Hyper-V instalado. Los detalles sobre estas nuevas API estarán disponibles a través de la documentación del proveedor WMI de [Hyper-V en MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

**Aplicaciones del lado invitado**

Los desarrolladores que escriben software para su uso dentro de una máquina virtual configurada para usar Memoria dinámica deben tener en cuenta que la memoria del sistema de máquina virtual ya no es constante. Por lo tanto, su aplicación debe liberar memoria cuando ya no sea necesario para permitir que otras aplicaciones aprovechen el recurso.

Las asignaciones de memoria y las desa asignaciones siguen funcionando de la forma habitual para las aplicaciones de usuario. Memoria dinámica es completamente transparente para la mayoría de las aplicaciones de usuario final. Sin embargo, si el software que se está desarrollando usa contadores de rendimiento de memoria en la máquina virtual, se deben realizar pruebas cuidadosas en un entorno habilitado para Memoria dinámica para asegurarse de que el software tiene en cuenta los cambios realizados en la asignación de memoria del sistema operativo invitado. La memoria disponible ya no es "estática" desde la perspectiva de la máquina virtual.

## <a name="solutions"></a>Soluciones

Las máquinas virtuales deben tener instalados los servicios de integración (SP1) actualizados para aprovechar las ventajas de Memoria dinámica. Asegúrese de que todas las máquinas que se usan en la administración de máquinas virtuales de Hyper-V usan los bits Windows Server 2008 R2 SP1 más recientes.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Memoria dinámica en el blog de Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Uso del proveedor WMI de Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Declinación de responsabilidades

La información contenida en este documento está relacionada con el producto de software de versión preliminar que se puede modificar considerablemente antes de su primera versión comercial. En consecuencia, es posible que la información no describa ni refleje con precisión el producto de software cuando se lanzó por primera vez comercialmente. Este documento es meramente informativo. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
