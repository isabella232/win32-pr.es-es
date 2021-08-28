---
description: Un paquete de 64 bits consta parcial o totalmente de componentes de 64 bits Windows Installer.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Paquetes del instalador de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540ef7afc5c70eeba2bb24eb376eae8e52b8e55cec2c8622ccdcf18a804b6f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559545"
---
# <a name="64-bit-windows-installer-packages"></a>Paquetes del instalador de Windows de 64 bits

Un paquete de 64 bits consta total o parcialmente de componentes de 64 [bits Windows Installer.](windows-installer-components.md) En la lista siguiente se identifican los requisitos de cada paquete de 64 Windows Installer:

-   El valor "Intel64" debe especificarse en el campo de plataforma de la propiedad [**Resumen**](template-summary.md) de plantilla si y solo si el paquete se ejecuta en un procesador Intel64 (Itanium).
-   El valor "x64" debe especificarse en el campo de plataforma de la propiedad [**Resumen**](template-summary.md) de plantilla si y solo si el paquete se ejecuta en un procesador x64.
-   El valor "Arm64" debe especificarse en el campo de plataforma de la propiedad [**Resumen**](template-summary.md) de plantilla si y solo si el paquete se ejecuta en un procesador Arm64.
-   La propiedad [**Resumen**](page-count-summary.md) de recuento de páginas debe establecerse en el entero 200 o superior, ya que Windows Installer 2.0 es la versión mínima capaz de instalar componentes de 64 bits. Los paquetes para la plataforma Arm64 requieren un valor de 500 o superior.
-   Cada componente del instalador de Windows de 64 bits del paquete debe incluir el bit **msidbComponentAttributes64bit** en la columna Atributos de la [tabla de componentes](component-table.md).

Para obtener más información, vea Windows Installer en sistemas operativos de [64](windows-installer-on-64-bit-operating-systems.md) bits y paquetes del instalador [de Windows de 32 bits.](32-bit-windows-installer-packages.md)

 

 



