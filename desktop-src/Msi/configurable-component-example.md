---
description: Este ejemplo permite al consumidor del módulo configurar de forma independiente un control de edición, el atributo checksum y el atributo Compressed.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Ejemplo de componente configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666675"
---
# <a name="configurable-component-example"></a>Ejemplo de componente configurable

En este ejemplo, las tablas ModuleConfiguration y ModuleSubstitution siguientes permiten al consumidor del módulo configurar de forma independiente el atributo de contraseña para un control de edición, el atributo de suma de comprobación para un archivo y el atributo comprimido para el mismo archivo.

[Tabla ModuleSubstitution](modulesubstitution-table.md)



| Tabla   | Row           | Columna     | Valor                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Edit1 | Atributos | \[= Contraseña\]                |
| Archivo    | Archivo1         | Atributos | \[= Checksum \] \[ = comprimido\] |



 

[Tabla ModuleConfiguration](moduleconfiguration-table.md)



| Nombre       | Formato   | Tipo | ContextData                              | DefaultValue | Atributos | DisplayName | Descripción |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Contraseña   | Bits |      | 2097152; True = 2097152; False = 0             | 0            | 0          |             |             |
| Suma de comprobación   | Bits |      | 1024; Suma de comprobación = 1024; Sin suma de comprobación = 0         | 0            | 0          |             |             |
| Compressed | Bits |      | 24576; Compressed = 16384; Sin comprimir = 8192 | 8192         | 0          |             |             |



 

 

 



