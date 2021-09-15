---
title: Método IWMPCdromAsync refreshStatus
description: El método refreshStatus actualiza la información de estado de la lista de reproducción de grabación actual.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Método refreshStatus Reproductor de Windows Media
- Método refreshStatus Reproductor de Windows Media , interfaz IWMPCdromAsync
- Interfaz IWMPCdromAsync Reproductor de Windows Media , método refreshStatus
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569009"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>IWMPCdromAsync::refreshStatus (método)

El **método refreshStatus** actualiza la información de estado de la lista de reproducción de grabación actual.

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

Debe llamar a este método después de crear o cambiar una lista de reproducción de grabación antes de leer la información de estado o de grabar el CD. Puede probar si se requiere una actualización obteniendo el valor **de burnState** y comprobando wmpbsRefreshStatusPending.

La actualización del estado es una operación sincrónica. Esto significa que puede transcurrir un largo período de tiempo antes de que este método vuelva si la lista de reproducción de grabación actual es grande y contiene muchos cambios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromIntegración.burnState (VB y C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**WMPState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





