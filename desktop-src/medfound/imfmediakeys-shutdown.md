---
description: 'Más información sobre: MÉTODO IMFMediaKeys::Shutdown'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: MÉTODO IMFMediaKeys::Shutdown
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 198eea5af6980828f6a85c9f4680812dbf4dbf0e3dbac2c5181c6347ffbf386e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114345"
---
# <a name="imfmediakeysshutdown-method"></a>MÉTODO IMFMediaKeys::Shutdown

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

**La** aplicación debe llamar al apagado antes de la versión final. En este momento se publica la referencia del Módulo de descifrado de contenido (CDM) y cualquier otro recurso. Sin embargo, las sesiones relacionadas no se liberan ni se cierran.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




