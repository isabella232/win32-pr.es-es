---
description: ICE75 comprueba que todas las acciones personalizadas de tipo de acción personalizada 17 (DLL), tipo de acción personalizada 18 (EXE), tipo de acción personalizada 21 (JScript) y tipo de acción personalizada 22 (VBScript) se secuencian después de la acción CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074543"
---
# <a name="ice75"></a>ICE75

ICE75 comprueba que todas las acciones personalizadas de tipo de acción [personalizada 17](custom-action-type-17.md) (DLL), tipo de acción personalizada [18](custom-action-type-18.md) (EXE), tipo de acción personalizada [21](custom-action-type-21.md) (JScript) y tipo de acción [personalizada 22](custom-action-type-22.md) (VBScript) se secuencian después de la [acción CostFinalize](costfinalize-action.md). Estos tipos de acción personalizada usan un archivo instalado como origen. ICE75 comprueba las tablas [InstallUISequence,](installuisequence-table.md) [InstallExecuteSequence Table,](installexecutesequence-table.md) [AdminUISequence Table](adminuisequence-table.md)y [AdminExecuteSequence](adminexecutesequence-table.md). Tenga en cuenta que la acción CostFinalize es necesaria en estas tablas de secuencia.

## <a name="result"></a>Resultado

ICE75 publica un error si encuentra una acción personalizada mediante un archivo instalado como un archivo de origen que no se secuencia después de la acción CostFinalize.

## <a name="example"></a>Ejemplo

ICE75 informa de los siguientes errores para el ejemplo que se muestra:

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción      | Tipo | Origen  |
|-------------|------|---------|
| ARCHIVO \_ DE ENTIDAD DE CERTIFICACIÓNExe | 18   | FileExe |
| \_FILEDLL de CA | 17   | FileDLL |



 

[Tabla AdminUISequence](adminuisequence-table.md) (parcial)



| Acción      | Secuencia |
|-------------|----------|
| ARCHIVO \_ DE ENTIDAD DE CERTIFICACIÓNExe | 1100     |



 

[Tabla AdminExecuteSequence](adminexecutesequence-table.md) (parcial)



| Acción       | Secuencia |
|--------------|----------|
| \_FILEDLL de CA  | 800      |
| CostFinalize | 1000     |



 

Para corregir los errores, ordene las acciones personalizadas después de la acción CostFinalize.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



