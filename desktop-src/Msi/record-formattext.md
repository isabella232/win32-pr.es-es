---
description: El método FormatText del objeto Record da formato a los campos según la plantilla del campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Método Record.FormatText
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
ms.openlocfilehash: 28170a4d92f656dcd12863eca5c003ccb851772f42de375e8f5f1b61a768ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626985"
---
# <a name="recordformattext-method"></a>Método Record.FormatText

El **método FormatText** del objeto [**Record**](record-object.md) da formato a los campos según la plantilla del campo 0.

## <a name="syntax"></a>Sintaxis


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **método FormatText** sigue la funcionalidad de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) si se pasó a **MsiFormatRecord** un identificador de instalador nulo como su primer parámetro. Como resultado, solo se procesan los parámetros del campo de registro y las propiedades no están disponibles para sustitución.

Por ejemplo, una cadena como "dar formato a este campo: 1 , dar formato a esta propiedad: propiedad " se resuelve para "dar formato a este campo: valor del campo 1, dar formato a esta \[ \] \[ \] propiedad: \[ propiedad \] ".

Los parámetros a los que [se va a](formatted.md) dar formato se incluyen entre corchetes... \[ \] . Los corchetes se pueden iterar porque las sustituciones se resuelven desde dentro hacia fuera.

Si una parte de la cadena está entre llaves { } y no contiene corchetes, se deja sin modificar, incluidas las llaves.

Tenga en cuenta que, en el caso [de](deferred-execution-custom-actions.md)las acciones personalizadas de ejecución aplazada, **FormatText** solo admite un conjunto limitado de propiedades: las propiedades CustomActionData y ProductCode. Para obtener más información, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Formato](formatted.md)
</dt> <dt>

[Tipos de datos de columna](column-data-types.md)
</dt> </dl>

 

 




