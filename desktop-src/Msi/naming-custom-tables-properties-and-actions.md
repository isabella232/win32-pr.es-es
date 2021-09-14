---
description: Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de tablas estándar, propiedades o acciones nativas del instalador de Windows.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Asignar nombres a tablas, propiedades y acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261068"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Asignar nombres a tablas, propiedades y acciones personalizadas

Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de tablas estándar, propiedades o acciones nativas del instalador de Windows.

Los autores de paquetes deben cumplir las siguientes directrices para los nombres de tabla, propiedad o acción personalizados.

-   Crear nombres para tablas personalizadas, propiedades o acciones que tengan un prefijo que identifique la aplicación.
-   Nunca use un nombre con Msi como prefijo. A partir de Windows Installer 2.0, todas las nuevas propiedades, acciones y tablas nativas del instalador de Windows reciben nombres precedido por Msi. Este prefijo no distingue mayúsculas de minúsculas, por ejemplo, MsiNewInternalTable. Dado que el prefijo no distingue mayúsculas de minúsculas, los autores deben evitar todos los casos del prefijo Msi.

Para obtener más información, vea [Nombres de tabla](table-names.md).

 

 



