---
title: IWMPCdromAsync startAsync (método)
description: El método startAsync abate el CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Método startAsync Reproductor de Windows Media
- Método startAsync Reproductor de Windows Media , interfaz IWMPCdromAsync
- Interfaz IWMPCdromAsync Reproductor de Windows Media método , startAsync
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7806501a619d6172d9f1ce0715045c822b30326c2b59c268f432708ea13923ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761075"
---
# <a name="iwmpcdromburnstartburn-method"></a>IWMPCdromAsync::startAsync (método)

El **método startAsync** abate el CD.

## <a name="syntax"></a>Sintaxis


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El valor de **burnstate** debe ser wmpbsReady o wmpbsStopped antes de llamar a este método.

Este método no funcionará si la unidad de CD no es un resalte o si el disco de la unidad no se puede escribir. Use **isAvailable para** determinar si un CD se puede inquiete.

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

[**IWMPCdromRom.isAvailable (VB y C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPCdromRom.stopRom (VB y C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





