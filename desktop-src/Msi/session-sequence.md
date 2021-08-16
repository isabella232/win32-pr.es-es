---
description: El método Sequence del objeto Session abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Método Session.Sequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 59e9bb09e66ad9a7bff51f1ce2e7e15750749d04a4d2f2c92365b78b29b34585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625123"
---
# <a name="sessionsequence-method"></a>Método Session.Sequence

El **método Sequence** del objeto [**Session**](session-object.md) abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence. Para cada fila capturada, se llama al [**método DoAction,**](session-doaction.md) siempre que cualquier expresión de condición proporcionada no se evalúe como False. Devuelve una enumeración msiDoActionStatusEnum, como se describe en el [**método DoAction.**](session-doaction.md)

## <a name="syntax"></a>Sintaxis


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*table* 
</dt> <dd>

Nombre de cadena necesario de la tabla que se usará para la secuenciación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Normalmente, las acciones de nivel superior llaman internamente a este método.

Una secuencia de acciones que contiene acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues,](writeregistryvalues-action.md) no se puede ejecutar llamando al **método Sequence.** La excepción a esta regla es si se llama al método **Sequence** desde una acción personalizada programada en la tabla [InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize.](costinitialize-action.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




