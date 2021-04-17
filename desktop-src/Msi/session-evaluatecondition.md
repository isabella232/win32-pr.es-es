---
description: El método EvaluateCondition del objeto de sesión evalúa una expresión lógica que contiene símbolos y valores. Este método usa la función MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Método Session. EvaluateCondition
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
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680409"
---
# <a name="sessionevaluatecondition-method"></a>Método Session. EvaluateCondition

El método **EvaluateCondition** del objeto de [**sesión**](session-object.md) evalúa una expresión lógica que contiene símbolos y valores. Este método usa la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .

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

Cadena requerida que contiene la expresión lógica. Para obtener más información, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un entero que indica la evaluación de la condición.



| Constante                  | Value | Descripción                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | La condición se evalúa como false.         |
| msiEvaluateConditionTrue  | 1     | La condición se evalúa como true.          |
| msiEvaluateConditionNone  | 2     | No se proporciona una expresión condicional. |
| msiEvaluateConditionError | 3     | La condición contiene un error de sintaxis.    |



 

## <a name="remarks"></a>Observaciones

Las expresiones condicionales se pueden usar para comparar los Estados de las características y los componentes. En la tabla siguiente se muestran los Estados de características y componentes que usa el método EvaluateCondition.



| Estado                 | Value | Descripción                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | No se realizó ninguna acción en la característica o componente.                 |
| msiInstallStateAbsent | 2     | La característica o componente no está presente.                     |
| msiInstallStateLocal  | 3     | La característica o componente está instalado en el equipo local. |
| msiInstallStateSource | 4     | La característica o componente está instalado para ejecutarse desde el origen.    |



 

> [!Note]  
> Los Estados no se establecen hasta que se llama al método [**SetInstallLevel**](session-setinstalllevel.md) , ya sea directamente o mediante la [acción CostFinalize](costfinalize-action.md). Por lo tanto, la comprobación de estado solo es útil en una expresión condicional en una tabla de secuencia de acciones.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
</dt> </dl>

 

 




