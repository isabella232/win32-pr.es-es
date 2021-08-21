---
description: El método EvaluateCondition del objeto Session evalúa una expresión lógica que contiene símbolos y valores. Este método usa la función MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Método Session.EvaluateCondition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fa5807314092c6245c23a329deb44a644ed54b22640292a06e08a9944f54e4dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629335"
---
# <a name="sessionevaluatecondition-method"></a>Método Session.EvaluateCondition

El **método EvaluateCondition** del [**objeto Session**](session-object.md) evalúa una expresión lógica que contiene símbolos y valores. Este método usa la [**función MsiEvaluateCondition.**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

## <a name="syntax"></a>Sintaxis


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*condition* 
</dt> <dd>

Cadena necesaria que contiene la expresión lógica. Para obtener más información, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un entero que indica la evaluación de la condición.



| Constante                  | Value | Descripción                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | La condición se evalúa como false.         |
| msiEvaluateConditionTrue  | 1     | La condición se evalúa como true.          |
| msiEvaluateConditionNone  | 2     | No se proporciona una expresión condicional. |
| msiEvaluateConditionError | 3     | La condición contiene un error de sintaxis.    |



 

## <a name="remarks"></a>Comentarios

Las expresiones condicionales se pueden usar para comparar los estados de características y componentes. En la tabla siguiente se muestran los estados de características y componentes que usa el método EvaluateCondition.



| Estado                 | Value | Descripción                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | No se ha realizado ninguna acción en la característica o el componente.                 |
| msiInstallStateAbsent | 2     | La característica o componente no está presente.                     |
| msiInstallStateLocal  | 3     | La característica o componente se instala en el equipo local. |
| msiInstallStateSource | 4     | La característica o componente se instala para ejecutarse desde el origen.    |



 

> [!Note]  
> Los estados no se establecen hasta que se llama [**al método SetInstallLevel,**](session-setinstalllevel.md) ya sea directamente o mediante [la acción CostFinalize](costfinalize-action.md). Por lo tanto, la comprobación de estado solo es útil en la expresión condicional en una tabla de secuencia de acciones.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
</dt> </dl>

 

 




