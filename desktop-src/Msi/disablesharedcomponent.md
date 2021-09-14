---
description: Si esta directiva de sistema por máquina está establecida en 1, ningún paquete del sistema obtiene la funcionalidad de componente compartido habilitada por el atributo msidbComponentAttributesShared en la tabla Component.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158535"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Si esta directiva [](system-policy.md) de sistema por máquina se establece en 1, ningún paquete del sistema obtiene la funcionalidad de componente compartido habilitada por el atributo **msidbComponentAttributesShared** en la tabla [Component](component-table.md). El valor predeterminado es 0, que habilita la funcionalidad de componentes compartidos para los componentes marcados con **msidbComponentAttributesShared** en todos los paquetes.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta función está disponible a partir de Windows Installer 4.5.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



