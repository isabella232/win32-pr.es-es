---
description: Un paquete de 64 bits se compone parcial o totalmente de componentes de Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Paquetes de Windows Installer de bits de 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909158"
---
# <a name="64-bit-windows-installer-packages"></a>Paquetes de Windows Installer de bits de 64

Un paquete de 64 bits se compone parcial o totalmente de componentes de [Windows Installer](windows-installer-components.md) de 64 bits. En la lista siguiente se identifican los requisitos para cada paquete de Windows Installer de 64 bits:

-   El valor "Intel64" debe especificarse en el campo Platform de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador Intel64 (Itanium).
-   El valor "x64" se debe escribir en el campo plataforma de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador x64.
-   El valor "Arm64" debe especificarse en el campo Platform de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador Arm64.
-   La propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) se debe establecer en el entero 200 o superior, porque Windows Installer 2,0 es la versión mínima que es capaz de instalar componentes de 64 bits. Los paquetes de la plataforma Arm64 requieren un valor de 500 o superior.
-   Cada componente de Windows Installer de 64 bits del paquete debe incluir el bit **msidbComponentAttributes64bit** en la columna Attributes de la [tabla de componentes](component-table.md).

Para obtener más información, consulte [Windows Installer en sistemas operativos de 64](windows-installer-on-64-bit-operating-systems.md) bits y [paquetes de Windows Installer de 32 bits](32-bit-windows-installer-packages.md).

 

 



