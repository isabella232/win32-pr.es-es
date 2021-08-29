---
description: ICE77 comprueba que las acciones personalizadas con el conjunto de bits msidbCustomActionTypeInScript se secuencian después de la acción InstallInitialize y antes de la acción InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b814a9cee6da87a76594949f2ad3250bbdd55c3666d0f500ea3a64ae3730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894985"
---
# <a name="ice77"></a>ICE77

ICE77 comprueba que las acciones personalizadas con el conjunto de bits **msidbCustomActionTypeInScript** se secuencian después de la acción [InstallInitialize](installinitialize-action.md) y antes de [la acción InstallFinalize](installfinalize-action.md). ICE77 comprueba la secuencia en las [tablas InstallExecuteSequence](installexecutesequence-table.md) y [AdminExecuteSequence](adminexecutesequence-table.md).

## <a name="result"></a>Resultado

ICE77 publica un error si se secuencia una acción personalizada en script antes de la acción InstallInitialize o después de la acción InstallFinalize.

ICE77 publica un error si falta la acción InstallInitialize o installFinalize.

## <a name="example"></a>Ejemplo

ICE77 notifica los siguientes errores para el ejemplo:

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción              | Tipo |
|---------------------|------|
| CA \_ InScriptInstall | 1025 |
| CA \_ InScriptAdmin   | 1026 |



 

[InstallExecuteSequence Table](installexecutesequence-table.md) (parcial)



| Acción              | Secuencia |
|---------------------|----------|
| CA \_ InScriptInstall | 2000     |
| InstallInitialize   | 1.500     |



 

[Tabla AdminExecuteSequence](adminexecutesequence-table.md) (parcial)



| Acción            | Secuencia |
|-------------------|----------|
| CA \_ InScriptAdmin | 1400     |
| InstallInitialize | 1.500     |
| InstallFinalize   | 6600     |



 

Para corregir los errores, secuencia las acciones personalizadas en script después de la acción InstallInitialize y antes de la acción InstallFinalize. Las acciones InstallInitialize e InstallFinalize deben estar presentes en la tabla InstallExecuteSequence y en la tabla AdminExecuteSequence.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



