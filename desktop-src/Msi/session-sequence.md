---
description: El método Sequence del objeto Session abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence (método)
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
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653974"
---
# <a name="sessionsequence-method"></a>Session. Sequence (método)

El método **Sequence** del objeto [**Session**](session-object.md) abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence. Para cada fila capturada, se llama al método [**OnAction**](session-doaction.md) , siempre que cualquier expresión de condición proporcionada no se evalúe como false. Devuelve una enumeración msiDoActionStatusEnum, tal y como se describe en el método [**OnAction**](session-doaction.md) .

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

Nombre de cadena requerido de la tabla que se va a utilizar para la secuenciación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Normalmente, se llama a este método internamente mediante acciones de nivel superior.

Una secuencia de acciones que contiene acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) , no se puede ejecutar llamando al método **Sequence** . La excepción a esta regla es si se llama al método de **secuencia** desde una acción personalizada programada en la [tabla InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md). Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




