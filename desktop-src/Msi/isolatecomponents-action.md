---
description: La acción IsolateComponents instala una copia de un componente (normalmente un archivo DLL compartido) en una ubicación privada para que la use una aplicación específica (normalmente un .exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Acción IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071998"
---
# <a name="isolatecomponents-action"></a>Acción IsolateComponents

La acción IsolateComponents instala una copia de un componente (normalmente un archivo DLL compartido) en una ubicación privada para que la use una aplicación específica (normalmente un .exe). Esto aísla la aplicación de otras copias del componente que se pueden instalar en una ubicación compartida del equipo. Para obtener más información, vea [Componentes aislados](isolated-components.md).

La acción hace referencia a cada registro de la tabla [IsolatedComponent](isolatedcomponent-table.md) y asocia los archivos del componente enumerados en el campo Componente compartido con el componente que aparece en el campo \_ Aplicación de \_ componentes. El instalador instala los archivos de Componente \_ compartido en el mismo directorio que la aplicación de \_ componentes. El instalador genera un archivo en este directorio, con una longitud de cero bytes, con el nombre de archivo corto del archivo de clave para la aplicación de componentes (normalmente es el mismo nombre de archivo que el .exe) anexado a \_ .local. La acción IsolatedComponent no afecta a la instalación de la aplicación \_ de componentes. Al desinstalar la aplicación de componentes también se quitan los archivos \_ \_ compartidos de componentes y el archivo .local del directorio.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción IsolateComponents solo se puede usar en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Esta acción debe ir después de la [acción CostInitialize](costinitialize-action.md) y antes de [la acción CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

Si la columna Condición de la acción IsolateComponents se evalúa como True o se deja en blanco, el instalador aísla todos los componentes enumerados en la [tabla IsolatedComponent](isolatedcomponent-table.md). Si la columna Condición se evalúa como False, el instalador omite la tabla IsolatedComponent y comparte los componentes habituales. La [**propiedad RedirectedDllSupport**](redirecteddllsupport.md) se puede usar para condición de esta acción. Para obtener más información, [vea Usar una tabla de secuencia.](using-a-sequence-table.md)

 

 



