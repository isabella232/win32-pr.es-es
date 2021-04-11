---
description: La acción IsolateComponents instala una copia de un componente (normalmente una DLL compartida) en una ubicación privada para su uso por parte de una aplicación específica (normalmente un archivo. exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Acción IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361395"
---
# <a name="isolatecomponents-action"></a>Acción IsolateComponents

La acción IsolateComponents instala una copia de un componente (normalmente una DLL compartida) en una ubicación privada para su uso por parte de una aplicación específica (normalmente un archivo. exe). Esto aísla la aplicación de otras copias del componente que se puede instalar en una ubicación compartida del equipo. Para obtener más información, vea [componentes aislados](isolated-components.md).

La acción hace referencia a cada registro de la [tabla IsolatedComponent](isolatedcomponent-table.md) y asocia los archivos del componente enumerados en el \_ campo compartido componente con el componente que aparece en el \_ campo aplicación de componentes. El instalador instala los archivos de componentes \_ compartidos en el mismo directorio que la aplicación de componentes \_ . El instalador genera un archivo en este directorio, de cero bytes de longitud y tiene el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ (normalmente, es el mismo nombre de archivo que el. exe) anexado con. local. La acción IsolatedComponent no afecta a la instalación de la \_ aplicación de componentes. Al desinstalar \_ la aplicación de componentes, también se quitan los \_ archivos compartidos del componente y el archivo. local del directorio.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción IsolateComponents solo se puede usar en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Esta acción debe aparecer después de la [acción CostInitialize](costinitialize-action.md) y antes de la [acción CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

Si la columna condición de la acción IsolateComponents se evalúa como true o se deja en blanco, el instalador aísla todos los componentes enumerados en la [tabla IsolatedComponent](isolatedcomponent-table.md). Si la columna condition se evalúa como false, el instalador omite la tabla IsolatedComponent y comparte los componentes de forma habitual. La propiedad [**RedirectedDllSupport**](redirecteddllsupport.md) se puede usar para condicionar esta acción. Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).

 

 



