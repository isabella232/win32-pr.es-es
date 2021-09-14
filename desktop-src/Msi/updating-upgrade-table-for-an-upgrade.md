---
description: Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad UpgradeCode, que se describe en Preparar una aplicación para futuras actualizaciones principales, y el paquete de actualización debe tener una tabla Upgrade.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Actualizar tabla de actualización para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254138"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Actualizar tabla de actualización para una actualización

Para aplicar una actualización principal mediante Windows Installer, el paquete de instalación del producto original debe especificar una propiedad [**UpgradeCode,**](upgradecode.md) que se describe en [Preparar](preparing-an-application-for-future-major-upgrades.md)una aplicación para futuras actualizaciones principales, y el paquete de actualización debe tener una tabla [Upgrade](upgrade-table.md).

Para obtener más información sobre las actualizaciones principales, vea [Actualizaciones principales](major-upgrades.md) en Revisiones [y actualizaciones.](patching-and-upgrades.md)

Al paquete de instalación MNP2000.msi se le asignó [**una propiedad UpgradeCode,**](upgradecode.md) como se describe en la sección [Especificación de propiedades](specifying-properties.md).

Windows El instalador aplica la actualización si el usuario ya ha instalado las versiones 1.0 a 1.4 (inclusive) del idioma inglés MNP2000. Windows El instalador migra toda la configuración de características del producto original al producto actualizado. El instalador quita los archivos que pertenecen a los productos originales que no se usan en la actualización del producto.

Si la copia de MNP2001.msi no incluye una tabla de [actualización,](upgrade-table.md)use Orca u otro editor de tablas para importar una tabla de actualización vacía en la base de datos desde Schema.msi. El SDK proporciona una copia de Schema.msi. Use el editor de bases de datos para MNP2001.msi y escriba los datos siguientes en la tabla de actualización vacía.



| UpgradeCode                            | VersionMin | VersionMax | Lenguaje | Atributos | Remove | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 3082     | 769        |        | OLDAPPFOUND    |



 

[Continuar](updating-properties-for-an-upgrade.md)

 

 



