---
description: Este ejemplo permite al consumidor del módulo configurar de forma independiente un control de edición, el atributo de suma de comprobación y el atributo comprimido.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Ejemplo de componente configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ff3e1567a19afd50a0ae2035893c027398816b535d5edfb233e89021ea9e59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500745"
---
# <a name="configurable-component-example"></a>Ejemplo de componente configurable

En este ejemplo, las siguientes tablas ModuleConfiguration y ModuleSubstitution permiten al consumidor del módulo configurar de forma independiente el atributo Password para un control de edición, el atributo de suma de comprobación de un archivo y el atributo comprimido para el mismo archivo.

[ModuleSubstitution Table](modulesubstitution-table.md)



| Tabla   | Fila           | Columna     | Valor                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Edit1 | Atributos | \[=Contraseña\]                |
| Archivo    | Archivo1         | Atributos | \[=Suma de comprobación \] \[ =Comprimido\] |



 

[Tabla ModuleConfiguration](moduleconfiguration-table.md)



| Nombre       | Formato   | Tipo | ContextData                              | DefaultValue | Atributos | DisplayName | Descripción |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Contraseña   | Campo de bits |      | 2097152; True=2097152; False=0             | 0            | 0          |             |             |
| Suma de comprobación   | Campo de bits |      | 1024; Checksum=1024; Sin suma de comprobación=0         | 0            | 0          |             |             |
| Compressed | Campo de bits |      | 24576; Compressed=16384; Uncompressed=8192 | 8192         | 0          |             |             |



 

 

 



