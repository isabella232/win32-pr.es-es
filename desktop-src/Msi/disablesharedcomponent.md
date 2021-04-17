---
description: Si esta Directiva del sistema por equipo está establecida en 1, ningún paquete del sistema obtiene la funcionalidad del componente compartido habilitada por el atributo msidbComponentAttributesShared en la tabla de componentes.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542742"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Si esta [Directiva del sistema](system-policy.md) por equipo está establecida en 1, ningún paquete del sistema obtiene la funcionalidad del componente compartido habilitada por el atributo **msidbComponentAttributesShared** en la [tabla de componentes](component-table.md). El valor predeterminado es 0, que habilita la funcionalidad de componentes compartidos para los componentes marcados con **msidbComponentAttributesShared** en todos los paquetes.

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible. Esta función está disponible a partir de Windows Installer 4,5.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 



