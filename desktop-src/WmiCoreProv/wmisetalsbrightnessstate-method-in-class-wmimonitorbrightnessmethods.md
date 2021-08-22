---
description: Se usa para controlar el estado de brillo del sensor de luz ambiente.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Método WmiSetALSBrightnessState de la clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051123"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Método WmiSetALSBrightnessState de la clase WmiMonitorBrightnessMethods

El **método WmiSetALSBrightnessState** se usa para controlar el estado de brillo del sensor de luz ambiente. Si se estableció una invalidación de brillo activa mediante el método [**WmiSetBrightness,**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) esa invalidación tendrá prioridad sobre el brillo de ALS establecido mediante este método. Para que una invalidación de brillo de ALS habilitada suba efecto, la directiva de brillo debe revertirse mediante el [**método WmiRevertToPolicyBrightness.**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*State* 
</dt> <dd>

Estado de brillo de ALS. False deshabilita la invalidación de brillo de ALS y true lo habilita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener más información sobre los códigos de [**error,**](/windows/desktop/WmiSdk/wmi-error-constants) vea Constantes de error WMI o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

