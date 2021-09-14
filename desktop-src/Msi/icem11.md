---
description: ICEM11 comprueba que un módulo de combinación configurable muestra la tabla ModuleConfiguration y la tabla ModuleSubstitution en la tabla ModuleIgnoreTable del módulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074472"
---
# <a name="icem11"></a>ICEM11

ICEM11 comprueba que un módulo de combinación configurable muestra la tabla [ModuleConfiguration](moduleconfiguration-table.md) y la tabla [ModuleSubstitution](modulesubstitution-table.md) en la [tabla ModuleIgnoreTable](moduleignoretable-table.md) del módulo. Esto garantiza que las herramientas de combinación que no reconocen módulos de combinación configurables (versión 2.0 anterior) no copian estas tablas en la base de datos de destino.

Este ICEM está disponible en el archivo Mergemod.cub proporcionado en el SDK de Windows Installer 2.0 y versiones posteriores. Para obtener más información, [consulte Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM11 publica un error si el módulo contiene una tabla ModuleConfiguration o ModuleSubstitution que no aparece en la tabla ModuleIgnoreTable.

## <a name="example"></a>Ejemplo

ICEM11 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (parcial)



| Nombre     | Formato | Tipo   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | Icono        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| Tabla   | Row              | Columna | Valor        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Texto   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Tabla               |
|---------------------|
| ModuleConfiguration |



 

Para corregir este error, incluya las tablas ModuleSubstitution y ModuleConfiguration en la tabla ModuleIgnoreTable.

## <a name="table-used-during-execution"></a>Tabla usada durante la ejecución

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



