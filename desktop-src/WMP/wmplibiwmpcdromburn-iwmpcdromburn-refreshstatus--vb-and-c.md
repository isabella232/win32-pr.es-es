---
title: IWMPCdromBurn refreshStatus, método
description: El método refreshStatus actualiza la información de estado de la lista de reproducción actual de la grabación.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- método refreshStatus de Windows Media Player
- método refreshStatus Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718827"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>IWMPCdromBurn:: refreshStatus (método)

El método **refreshStatus** actualiza la información de estado de la lista de reproducción actual de la grabación.

## <a name="syntax"></a>Sintaxis


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Debe llamar a este método después de crear o cambiar una lista de reproducción de grabación antes de leer la información de estado o grabar el CD. Puede comprobar si se requiere una actualización obteniendo el valor de **burnState** y comprobando si hay wmpbsRefreshStatusPending.

La actualización del estado es una operación sincrónica. Esto significa que puede transcurrir un período largo de tiempo antes de que este método devuelva si la lista de reproducción actual de la grabación es grande y contiene muchos cambios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. burnState (VB y C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





