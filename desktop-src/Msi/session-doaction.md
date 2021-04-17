---
description: El método OnAction del objeto de sesión ejecuta la función de acción correspondiente al nombre proporcionado.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Método Session. OnAction (fotoadquisición. h)
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
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680410"
---
# <a name="sessiondoaction-method"></a>Session. OnAction (método)

El método **OnAction** del objeto de [**sesión**](session-object.md) ejecuta la función de acción correspondiente al nombre proporcionado. Si se proporciona un nombre de acción nulo, el motor utiliza el valor en mayúsculas de la [propiedad Action](action.md) como la acción que se va a realizar. Si no se define ningún valor de propiedad, se realiza la acción predeterminada, que se define actualmente como INSTALL. Este método devuelve una enumeración de enteros.

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

Nombre de cadena requerido de la acción que se va a ejecutar. Distingue mayúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) , no se pueden ejecutar llamando al método **OnAction** . La excepción a esta regla es si se llama al método **OnAction** desde una acción personalizada programada en la [tabla InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md). Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Encabezado<br/>  | <dl> <dt>Fotoadquisición. h</dt> </dl>                                                                                                                                                               |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




