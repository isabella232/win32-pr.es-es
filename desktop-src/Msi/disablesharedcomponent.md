---
description: Si esta directiva de sistema por máquina está establecida en 1, ningún paquete del sistema obtiene la funcionalidad de componente compartido habilitada por el atributo msidbComponentAttributesShared en la tabla Component.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7576406e14b0f9ac48a26735b984302c2d765b784484022a85ec50244ee8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143106"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Si esta directiva [](system-policy.md) de sistema por máquina se establece en 1, ningún paquete del sistema obtiene la funcionalidad de componente compartido habilitada por el atributo **msidbComponentAttributesShared** en la tabla [Component](component-table.md). El valor predeterminado es 0, que habilita la funcionalidad de componentes compartidos para los componentes marcados con **msidbComponentAttributesShared** en todos los paquetes.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta función está disponible a partir de Windows Installer 4.5.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



