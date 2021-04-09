---
description: Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad UpgradeCode, descrita en preparación de una aplicación para futuras actualizaciones principales, y el paquete de actualización debe tener una tabla de actualización.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Actualizando la tabla de actualización para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156041"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Actualizando la tabla de actualización para una actualización

Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad [**UpgradeCode**](upgradecode.md) , descrita en [preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md), y el paquete de actualización debe tener una [tabla de actualización](upgrade-table.md).

Para obtener más información acerca de las actualizaciones principales, consulte [actualizaciones principales](major-upgrades.md) en [revisiones y actualizaciones](patching-and-upgrades.md).

Al paquete de instalación de MNP2000.msi se le asignó una propiedad [**UpgradeCode**](upgradecode.md) , como se describe en la sección [especificar propiedades](specifying-properties.md).

Windows Installer aplica la actualización si el usuario ya ha instalado las versiones 1,0 a 1,4 (inclusivas) del idioma inglés MNP2000. Windows Installer migra la configuración de las características del producto original al producto actualizado. El instalador quita los archivos que pertenecen a los productos originales que no se usan en la actualización del producto.

Si su copia de MNP2001.msi no incluye una [tabla de actualización](upgrade-table.md), utilice Orca u otro editor de tablas para importar una tabla de actualización vacía en la base de datos de Schema.msi. El SDK proporciona una copia de Schema.msi. Utilice el editor de base de datos para abrir MNP2001.msi y escriba los datos siguientes en la tabla de actualización vacía.



| UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos | Remove | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 3082     | 769        |        | OLDAPPFOUND    |



 

[Continuar](updating-properties-for-an-upgrade.md)

 

 



