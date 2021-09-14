---
description: En el ejemplo siguiente se muestra cómo Windows Installer 3.0 y versiones posteriores para aplicar revisiones en el orden en que se crearon.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Ejemplo de varias revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074341"
---
# <a name="multiple-patching-example"></a>Ejemplo de varias revisiones

En el ejemplo siguiente se muestra cómo Windows Installer 3.0 y versiones posteriores para aplicar revisiones en el orden en que se crearon.

## <a name="example"></a>Ejemplo

En este ejemplo hay tres revisiones, QFE1, QFE2 y ServicePack1, y cada una tiene una [tabla MsiPatchSequence.](msipatchsequence-table.md) Estas revisiones se han escrito para aplicarse a la versión 1.0 de la aplicación.



| Nombre de revisión   | Tipo de revisión    | Sequence Number |
|--------------|---------------|-----------------|
| QFE1         | Actualización pequeña  | 1.1.0           |
| QFE2         | Actualización pequeña  | 1.2.0           |
| ServicePack1 | Actualización secundaria | 1.3.0           |



 

La [tabla MsiPatchSequence](msipatchsequence-table.md) de cada revisión solo tiene un registro que contiene la familia de revisiones, el código de producto y el número de secuencia. Las tres revisiones se aplican al mismo producto y pertenecen a la misma familia de revisiones, denominada AppPatch. Ninguna de las revisiones tiene el **atributo msidbPatchSequenceSupersedeEarlier.**

[Tabla MsiPatchSequence para](msipatchsequence-table.md) la actualización pequeña de QFE1. [](small-updates.md) 

| PatchFamily | ProductCode                            | Secuencia | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Tabla MsiPatchSequence para](msipatchsequence-table.md) la actualización pequeña de QFE2. [](small-updates.md) 

| PatchFamily | ProductCode                            | Secuencia | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md). 

| PatchFamily | ProductCode                            | Secuencia | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Si un usuario instala la versión 1.0 del producto y, a continuación, aplica QFE2 y, posteriormente, decide aplicar QFE1, Windows Installer garantiza que la secuencia efectiva de aplicación de revisión al producto es QFE1 aplicada antes que QFE2. Si el usuario aplica ServicePack1 y, a continuación, aplica QFE2 y QFE1 juntos en una fecha posterior, el instalador de Windows garantiza que la secuencia efectiva de aplicación de revisión al producto sea QFE1 por delante de QFE2 y por delante de ServicePack1.

Si ServicePack1 tiene **msidbPatchSequenceSupersedeEarlier** establecido en la columna Atributos de su tabla [MsiPatchSequence,](msipatchsequence-table.md) significa que el Service Pack contiene todos los cambios en QFE1 y QFE2. En este caso, QFE1 y QFE2 no se aplican cuando se aplica ServicePack1.

**Windows Installer 2.0:** No se admite. Las versiones anteriores Windows Installer 3.0 solo pueden instalar una revisión por transacción y las revisiones se aplican en la secuencia que se proporcionan. En el ejemplo anterior, si QFE2 se aplica primero y luego se aplica QFE1, son dos transacciones y las revisiones se aplican a la versión 1.0 de la aplicación en la secuencia QFE2 seguida de QFE1. Si primero se aplica ServicePack1, QFE1 o QFE2 no se pueden aplicar en una transacción posterior porque ServicePack1 es una actualización secundaria que cambia la versión de la aplicación. QFE1 y QFE2 solo se pueden aplicar a la versión 1.0 de la aplicación.

 

 



