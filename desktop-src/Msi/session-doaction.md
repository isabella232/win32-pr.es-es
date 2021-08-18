---
description: El método DoAction del objeto Session ejecuta la función de acción correspondiente al nombre proporcionado.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Método Session.DoAction (Photoacquire.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629395"
---
# <a name="sessiondoaction-method"></a>Método Session.DoAction

El **método DoAction** del [**objeto Session**](session-object.md) ejecuta la función de acción correspondiente al nombre proporcionado. Si se proporciona un nombre de acción NULL, el motor usa el valor en mayúsculas de la [propiedad ACTION](action.md) como acción que se va a realizar. Si no se define ningún valor de propiedad, se realiza la acción predeterminada, definida actualmente como INSTALL. Este método devuelve una enumeración de enteros.

## <a name="syntax"></a>Sintaxis


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*action* 
</dt> <dd>

Nombre de cadena necesario de la acción que se ejecutará. Distingue mayúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues,](writeregistryvalues-action.md) no se pueden ejecutar llamando al **método DoAction.** La excepción a esta regla es si se llama al método **DoAction** desde una acción personalizada programada en la tabla [InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize.](costinitialize-action.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Header<br/>  | <dl> <dt>Photoacquire.h</dt> </dl>                                                                                                                                                               |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




