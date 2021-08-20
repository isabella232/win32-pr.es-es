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
ms.openlocfilehash: 1cd3ecbd249f9731993c541dcee33f81142e042185ca4bba0325af942fd42394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930645"
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

## <a name="remarks"></a>Comentarios

Debe llamar a este método después de crear o cambiar una lista de reproducción de grabación antes de leer la información de estado o grabar el CD. Puede probar si se requiere una actualización obteniendo el valor **de burnState** y comprobando wmpbsRefreshStatusPending.

La actualización del estado es una operación sincrónica. Esto significa que puede transcurrir un largo período de tiempo antes de que este método vuelva si la lista de reproducción de grabación actual es grande y contiene muchos cambios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromIntegración.burnState (VB y C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**WMPState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





