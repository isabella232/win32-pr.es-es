---
description: El método FormatText del objeto record da formato a los campos según la plantilla del campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Método record. FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653834"
---
# <a name="recordformattext-method"></a>Método record. FormatText

El método **FormatText** del objeto [**Record**](record-object.md) da formato a los campos según la plantilla del campo 0.

## <a name="syntax"></a>Sintaxis


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **FormatText** sigue la funcionalidad de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) si se pasa a **MsiFormatRecord** un identificador de instalador NULL como su primer parámetro. Como resultado, solo se procesan los parámetros de campo de registro y las propiedades no están disponibles para la sustitución.

Por ejemplo, una cadena como "dar formato a este campo: \[ 1 \] , dar formato a esta propiedad \[ \] " se resuelve como "dar formato a este campo: valor de campo 1, dar formato a esta propiedad: \[ propiedad \] ".

Los parámetros a los que se va a [dar formato](formatted.md) se incluyen entre corchetes \[ ... \] . Los corchetes se pueden iterar porque las sustituciones se resuelven desde el interior.

Si una parte de la cadena está entre llaves {} y no contiene corchetes, se deja sin cambios, incluidas las llaves.

Nota en el caso de [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md), **FormatText** solo admite un conjunto limitado de propiedades: las propiedades CustomActionData y ProductCode. Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Formatea](formatted.md)
</dt> <dt>

[Tipos de datos de columna](column-data-types.md)
</dt> </dl>

 

 




